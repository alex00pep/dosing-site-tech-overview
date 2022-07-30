# Browser support

Material for MkDocs goes at great lengths to support the largest possible range
of browsers while retaining the simplemost possibilities for customization via
modern CSS features like [custom properties] and [mask images].

  [custom properties]: https://caniuse.com/css-variables
  [mask images]: https://caniuse.com/mdn-css_properties_mask-image

## Supported browsers

The following table lists all browsers for which Material for MkDocs offers full
support, so it can be assumed that all features work without degradation. If you
find a feature not to be working in a browser in the supported version range,
please [open an issue]:



Browser support matrix sourced from [caniuse.com].[^1]

  [^1]:
    The data was collected from [caniuse.com] in January 2022, and is primarily
    based on browser support for [custom properties], [mask images] and the
    [:is pseudo selector] which are not entirely polyfillable. Browsers with a
    cumulated market share of less than 1% were not considered, but might still
    be fully or partially supported.

Note that the usage data is based on global browser market share, so it could
in fact be entirely different for your target demographic. It's a good idea to
check the distribution of browser types and versions among your users.

  [open an issue]: https://github.com/squidfunk/mkdocs-material/issues/new/choose
  [caniuse.com]: https://caniuse.com/
  [:is pseudo selector]: https://caniuse.com/css-matches-pseudo

## Other browsers

Albeit your site might not look as perfect as when viewed with a modern browser,
the following older browser versions might work with some additional effort:

- :fontawesome-brands-firefox: __Firefox 31-52__ – icons will render as little
  boxes due to missing support for [mask images]. While this cannot be
  polyfilled, it might be mitigated by hiding the icons altogether.
- :fontawesome-brands-edge: __Edge 16-18__ – the spacing of some elements might
  be a little off due to missing support for the [:is pseudo selector], which
  can be mitigated with some additional effort.
- :fontawesome-brands-internet-explorer: __Internet Explorer__ - no support,
  mainly due to missing support for [custom properties]. The last version of
  Material for MkDocs to support Internet Explorer is
  [:octicons-tag-24: 4.6.3][IE support].

  [IE support]: https://github.com/squidfunk/mkdocs-material/releases/tag/4.6.3