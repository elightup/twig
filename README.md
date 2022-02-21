This is a mirror of `twig/twig` which is used to prevent conflicts when other plugins use a different version of Twig inside WordPress.

This package is used in:

- [MB Views](https://metabox.io/plugins/mb-views/)
- [Meta Box Builder](https://metabox.io/plugins/meta-box-builder/)
- [Slim SEO Schema](https://metabox.io/plugins/slim-seo-schema/)

Making this package helps reduce duplication, especially in Meta Box AIO.

To make it less confusing, the version of this package is the same as Twig.

This package is created using [Mozart](https://github.com/coenjacobs/mozart), a briliant tool for WordPress developers.

## How to build the package

Install mozart globally

Run the following commands:

```
composer require twig/twig
mozart compose
```

## Usage

Instead if use a `Twig` class like `Twig\ClassName`, you need to prepend `eLightup\` to the class name, e.g.: `eLightUp\Twig\ClassName`.