# `\a` `external` argument

↑ **Parent:** [`\a` argument](a-argument.md)  
🏷️ **Tags:** [Boolean argument](boolean-argument.md)

If given and true, forces a the link to be an [external link](external-link.md).

Otherwise, the external is automatically guessed based on the address given as explained at [Section "External link"](external-link.md).

Common use cases for the `external` argument is to link to non OurBigBook content in the current domain, e.g.:
- [link to the domain root path](link-to-the-domain-root-path.md) for [Subdirectory deployments](subdirectory-deployment.md)
- link non OurBigBook subdirectories. E.g., [https://github.com/cirosantilli/cirosantilli.github.io/blob/master/index.bigb](https://github.com/cirosantilli/cirosantilli.github.io/blob/master/index.bigb) was rendered at [https://cirosantilli.com](https://cirosantilli.com), and contains links `\a[markdown-style-guide]{external}` to [https://cirosantilli.com/markdown-style-guide](https://cirosantilli.com/markdown-style-guide), whose source lives in a separate non-OurBigBook repository: [https://github.com/cirosantilli/markdown-style-guide/](https://github.com/cirosantilli/markdown-style-guide/)

**Table of contents**

- [Link to the domain root path](link-to-the-domain-root-path.md)
- [Subdirectory deployment](subdirectory-deployment.md)
- [External link](external-link.md)
  - [Internal path links are smart](internal-path-links-are-smart.md)
- [`_dir` directory](dir-directory.md)
- [`_file` output directory](file-output-directory.md)
- [`_raw` directory](raw-directory.md)
- [URL with protocol](url-with-protocol.md)

## ↑ Ancestors (5)

1. [`\a` argument](a-argument.md)
2. [Link](link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [`\a` `href` argument](a-href-argument.md)
- [Features](features.md)
- [Image `external` argument](image-external-argument.md)
- [Link to the domain root path](link-to-the-domain-root-path.md)
