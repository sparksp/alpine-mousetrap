> ✨ Help support the maintenance of this package by [sponsoring me](https://github.com/sponsors/danharrin).

# Alpine.js Mousetrap

A simple library for handling keyboard shortcuts.

![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/danharrin/alpine-mousetrap?label=version&style=flat-square)
![Build size Brotli](https://img.badgesize.io/danharrin/alpine-mousetrap/master/dist/alpine-mousetrap.js.svg?compression=gzip&style=flat-square&color=green)
[![Monthly downloads via CDN](https://data.jsdelivr.com/v1/package/npm/@danharrin/alpine-mousetrap/badge)](https://www.jsdelivr.com/package/npm/@danharrin/alpine-mousetrap)

## About

This plugin adds a new `x-mousetrap` directive to all of your Alpine components that can be used to register keyboard shortcuts.

## Installation

### CDN

Include the following `<script>` tag in the `<head>` of your document, just before Alpine.

```html
<script src="https://cdn.jsdelivr.net/npm/@danharrin/alpine-mousetrap@0.x.x/dist/alpine-mousetrap.js" defer></script>
```

### NPM

```bash
npm install @danharrin/alpine-mousetrap --save-dev
```

Add the `x-mousetrap` directive to your project by importing the package **before** Alpine.js.

```js
import Alpine from 'alpinejs'
import Mousetrap from '@danharrin/alpine-mousetrap'

Alpine.plugin(Mousetrap)

window.Alpine = Alpine
window.Alpine.start()
```

## Usage

To register keyboard shortcuts for a button or other clickable element:

```html
<div x-data="{}">
    <button
        type="button"
        x-mousetrap.command+k.ctrl+k
    >
        Button
    </button>
</div>
```

The list of keyboard shortcuts should be written as per [Mousetrap](https://github.com/ccampbell/mousetrap)'s documentation, each separated by a period `.`.

Alternatively, you can invoke a custom function when the keyboard shortcut is made:

```html
<div x-data="{}">
    <button
        type="button"
        x-mousetrap.command+k.ctrl+k="console.log('command k or control k')"
    >
        Button
    </button>
</div>
```

## Versioning

This projects follow the [Semantic Versioning](https://semver.org/) guidelines.

## License

Copyright (c) Dan Harrin

Licensed under the MIT license, see [LICENSE.md](LICENSE.md) for details.
