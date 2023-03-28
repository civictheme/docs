# Spacing

### Particle

Particle is the most basic unit of measurement,  using pixels to tie to the design grid which is in pixels as well.&#x20;

Depending on the context, most of the values will be using conversion to rem with the `rem()` function.&#x20;

`ct-particle()` function can be used to baseelement measurements off the particle.

For spacing, use `ct-spacing()` function instead.

### Spacing

Spacing (such as margin or padding) can be applied using the `ct-spacing()` function.

Spacing size is defined in `$ct-spacing` variable and defaults to `ct-particle()`

```scss
div {
  padding: ct-spacing(1) ct-spacing(2);
  margin-bottom: ct-spacing(2);
}
```

