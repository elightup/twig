This is a mirror of `twig/twig` which is used to prevent conflicts when other plugins use a different version of Twig inside WordPress.

This package is used in:

- [MB Views](https://metabox.io/plugins/mb-views/)
- [MB Builder](https://metabox.io/plugins/meta-box-builder/)
- [Slim SEO](https://wpslimseo.com)
- [Slim SEO Pro](https://wpslimseo.com/products/slim-seo-pro/)

Making this package helps reduce duplication, especially in [Meta Box AIO](https://metabox.io/aio/).

To make it less confusing, the version of this package is the same as Twig.

This package is created using [Mozart](https://github.com/coenjacobs/mozart), a briliant tool for WordPress developers.

## How to build the package

Install mozart globally

Run the following commands:

```
composer require twig/twig
```

Notes for the build:

- Twig 3.11.3 is the last version that supports PHP 7.4 (3.12+ requires PHP 8). `config.platform.php` is set to 7.4 so Composer picks dependencies that run on PHP 7.4 (e.g. `symfony/deprecation-contracts` 2.5, not 3.x which uses the `mixed` type).
- Twig 3.11.3 has security advisories that are fixed only in Twig 3.26+ (PHP 8.1+). Most affect the sandbox, which Meta Box plugins do not use, and templates are written by admins. `audit.block-insecure` is off so Composer can install it.

## Usage

Instead if use a `Twig` class like `Twig\ClassName`, you need to prepend `eLightup\` to the class name, e.g.: `eLightUp\Twig\ClassName`.

## Notes

The package includes a `twig.php` file, which acts like a plugin bootstrap file for WordPress. This helps you just enable this plugin inside WordPress for testing before bundling it into plugins.