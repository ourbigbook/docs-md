# Arbitrary code execution

↑ **Parent:** [Security](security.md)

OurBigBook is designed to not allow arbitrary code execution by default on any [OurBigBook CLI](ourbigbook-cli.md) command.

This means that it it should be safe to just download any untrusted OurBigBook repository, and convert it with [OurBigBook CLI](ourbigbook-cli.md), even if you don't trust its author.

In order to allow code execution for pre/post processing tasks e.g. from [`prepublish`](ourbigbook-json/prepublish.md), use the [`--unsafe-ace`](unsafe-ace.md) option.

Note however that you have to be careful in general, since e.g. a malicious author could create a package with their own malicious version of the `ourbigbook` executable, that you could unknowingly run with with the standard `npx ourbigbook` execution.

## ↑ Ancestors (2)

1. [Security](security.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`--unsafe-ace`](unsafe-ace.md)
