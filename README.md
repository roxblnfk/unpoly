<p align="center">Remove unnecessary PHP polyfills</p>

<div align="center">

[![Sponsor](https://img.shields.io/static/v1?style=for-the-badge&label=&message=Patreon&logo=patreon&logoColor=white&color=%23F96854)](https://patreon.com/roxblnfk)

</div>

<br />

Composer installs `symfony/polyfill-php*` packages even when the PHP version already has every function they backport. This metapackage declares them as replaced, so Composer skips them and the autoloader stops loading dead code.

## Get Started

### Installation

```bash
composer require roxblnfk/unpoly
```

[![PHP](https://img.shields.io/packagist/dependency-v/roxblnfk/unpoly/php.svg?style=flat-square&logo=php)](https://packagist.org/packages/roxblnfk/unpoly)
[![Latest Version on Packagist](https://img.shields.io/packagist/v/roxblnfk/unpoly.svg?style=flat-square&logo=packagist)](https://packagist.org/packages/roxblnfk/unpoly)
[![License](https://img.shields.io/packagist/l/roxblnfk/unpoly.svg?style=flat-square)](LICENSE)
[![Total Downloads](https://img.shields.io/packagist/dt/roxblnfk/unpoly.svg?style=flat-square)](https://packagist.org/packages/roxblnfk/unpoly/stats)

### Versions

A version `1.8.X.N` requires PHP `>= 8.X` and replaces the polyfill of PHP 8.X plus the `N` previous PHP versions:

| Version   | Requires PHP | Replaces polyfills |
|-----------|--------------|--------------------|
| `1.8.6.0` | `>= 8.6`     | 8.6                |
| `1.8.6.1` | `>= 8.6`     | 8.5 .. 8.6         |
| `1.8.6.6` | `>= 8.6`     | 8.0 .. 8.6         |
| `1.8.6.8` | `>= 8.6`     | 7.3 .. 8.6         |

Composer picks the newest version your PHP allows, which replaces the widest range of polyfills published for that PHP. Pin a lower `N` only to keep some polyfills installed.
