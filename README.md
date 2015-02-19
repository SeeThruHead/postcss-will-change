# PostCSS Will Change [![Build Status](https://travis-ci.org/postcss/postcss-will-change.svg)](https://travis-ci.org/postcss/postcss-will-change)

[PostCSS] plugin to insert 3D hack before will-change property.

This plugin uses `backface-visibility` to has prevent overriding
more popular `transform` property.

Use this plugin only before [Autoprefixer]. It will add vendor prefixes
to `backface-visibility`.

[Autoprefixer]: https://github.com/postcss/autoprefixer
[PostCSS]:      https://github.com/postcss/postcss

```css
.foo {
    will-change: transform;
}
```

```css
.foo {
    backface-visibility: hidden;
    will-change: transform;
}
```

## Usage

```js
postcss([ require('postcss-will-change') ])
```

See [PostCSS] docs for examples for your environment.