# `\JsCanvasDemo`

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [XSS unsafe macro](xss-unsafe-macro.md)

The `JsCanvasDemo` macro allows you to create interactive HTML/JavaScript [canvas](https://en.wikipedia.org/wiki/Canvas_element) demos easily.

These demos:
- only start running when the user scrolls over them for the first time
- stop automatically when they leave the viewport
so you can stuff as many of them as you want on a page, and they won't cause the reader's CPU to fry an egg.


```
\JsCanvasDemo[[
new class extends OurbigbookCanvasDemo {
  init() {
    super.init('hello');
    this.pixel_size_input = this.addInputAfterEnable(
      'Pixel size',
      {
        'min': 1,
        'type': 'number',
        'value': 1,
      }
    );
  }
  draw() {
    var pixel_size = parseInt(this.pixel_size_input.value);
    for (var x = 0; x < this.width; x += pixel_size) {
      for (var y = 0; y < this.height; y += pixel_size) {
        var b = ((1.0 + Math.sin(this.time * Math.PI / 16)) / 2.0);
        this.ctx.fillStyle =
          'rgba(' +
          (x / this.width) * 255 + ',' +
          (y / this.height) * 255 + ',' +
          b * 255 +
          ',255)'
        ;
        this.ctx.fillRect(x, y, pixel_size, pixel_size);
      }
    }
  }
}
]]
```
which renders as:



> new class extends OurbigbookCanvasDemo {
>   init() {
>     super.init('hello');
>     this.pixel\_size\_input = this.addInputAfterEnable(
>       'Pixel size',
>       {
>         'min': 1,
>         'type': 'number',
>         'value': 1,
>       }
>     );
>   }
>   draw() {
>     var pixel\_size = parseInt(this.pixel\_size\_input.value);
>     for (var x = 0; x \< this.width; x += pixel\_size) {
>       for (var y = 0; y \< this.height; y += pixel\_size) {
>         var b = ((1.0 + Math.sin(this.time \* Math.PI / 16)) / 2.0);
>         this.ctx.fillStyle =
>           'rgba(' +
>           (x / this.width) \* 255 + ',' +
>           (y / this.height) \* 255 + ',' +
>           b \* 255 +
>           ',255)'
>         ;
>         this.ctx.fillRect(x, y, pixel\_size, pixel\_size);
>       }
>     }
>   }
> }

And another one showing off some [WebGL](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API):

new class extends OurbigbookCanvasDemo {
  init() {
    super.init('webgl', {context\_type: 'webgl'});
    this.ctx.viewport(0, 0, this.ctx.drawingBufferWidth, this.ctx.drawingBufferHeight);
    this.ctx.clearColor(0.0, 0.0, 0.0, 1.0);
    this.vertexShaderSource = \`
\#version 100
precision highp float;
attribute float position;
void main() {
  gl\_Position = vec4(position, 0.0, 0.0, 1.0);
  gl\_PointSize = 64.0;
}
\`;

    this.fragmentShaderSource = \`
\#version 100
precision mediump float;
void main() {
  gl\_FragColor = vec4(0.18, 0.0, 0.34, 1.0);
}
\`;
    this.vertexShader = this.ctx.createShader(this.ctx.VERTEX\_SHADER);
    this.ctx.shaderSource(this.vertexShader, this.vertexShaderSource);
    this.ctx.compileShader(this.vertexShader);
    this.fragmentShader = this.ctx.createShader(this.ctx.FRAGMENT\_SHADER);
    this.ctx.shaderSource(this.fragmentShader, this.fragmentShaderSource);
    this.ctx.compileShader(this.fragmentShader);
    this.program = this.ctx.createProgram();
    this.ctx.attachShader(this.program, this.vertexShader);
    this.ctx.attachShader(this.program, this.fragmentShader);
    this.ctx.linkProgram(this.program);
    this.ctx.detachShader(this.program, this.vertexShader);
    this.ctx.detachShader(this.program, this.fragmentShader);
    this.ctx.deleteShader(this.vertexShader);
    this.ctx.deleteShader(this.fragmentShader);
    if (!this.ctx.getProgramParameter(this.program, this.ctx.LINK\_STATUS)) {
      console.log('error ' + this.ctx.getProgramInfoLog(this.program));
      return;
    }
    this.ctx.enableVertexAttribArray(0);
    var buffer = this.ctx.createBuffer();
    this.ctx.bindBuffer(this.ctx.ARRAY\_BUFFER, buffer);
    this.ctx.vertexAttribPointer(0, 1, this.ctx.FLOAT, false, 0, 0);
    this.ctx.useProgram(this.program);
  }
  draw() {
    this.ctx.clear(this.ctx.COLOR\_BUFFER\_BIT);
    this.ctx.bufferData(this.ctx.ARRAY\_BUFFER, new Float32Array(\[Math.sin(this.time / 60.0)\]), this.ctx.STATIC\_DRAW);
    this.ctx.drawArrays(this.ctx.POINTS, 0, 1);
  }
}One day, I believe, one day, humanity shall invent a way to sandbox JavaScript execution so that this will cease to be an [XSS unsafe macro](xss-unsafe-macro.md): 
- [https://stackoverflow.com/questions/12209657/how-can-i-sandbox-untrusted-user-submitted-javascript-content](https://stackoverflow.com/questions/12209657/how-can-i-sandbox-untrusted-user-submitted-javascript-content)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)
