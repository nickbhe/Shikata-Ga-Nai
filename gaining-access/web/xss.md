# XSS

You can check an input field with these symbols: \[ &lt; &gt; ‘ “ { } ; \], if they are not removed or encoded the field might be vulnerable to XSS.

## XSS Types

* **Stored XSS** \[Persistent XSS\] occurs when the injection is stored and displayed to everyone.

  \*\*\*\*

* **Reflected XSS** includes payload from an outer source, like a link or request.
* **DOM-based** happens within the page’s DOM.

## Injection Methods

### Iframe Injection

Example:

![](https://lh5.googleusercontent.com/GJuvdT2p5AKlv7fE9WAezMVa0_tVITCfKL1e0f0u2J5QXFyUcUzKjs2I8puEFKkbcEbeJyNOaYWCoKgA6D-rOqNR21adICerHBT-sW-F_ZFuOqoCREjVTSWIlcih0lu3sR_IwP4O)

Every user that will enter the site will send us a request!

