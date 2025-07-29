# Digest::AutoLoader

[![License](https://img.shields.io/badge/license-Artistic%201.0%20OR%20GPL--1.0%2B-blue.svg)](https://dev.perl.org/licenses/)
[![CPAN version](https://badge.fury.io/pl/Digest-AutoLoader.svg)](https://metacpan.org/pod/Digest::AutoLoader)

A simple frontend module for autoloading various `Digest::` modules in Perl.

## Overview

`Digest::AutoLoader` is a lightweight helper module that simplifies loading of common `Digest::` modules dynamically at runtime. It also documents the standard interface expected from all `Digest::` modules, ensuring consistency and easier usage for developers.

This module is intended for use with Perl 5.004 or newer.

## Features

- 🧩 **Autoloading**: Automatically loads `Digest::MD5`, `Digest::SHA1`, or any other supported module on demand.
- 📚 **Unified Interface**: Provides standardized documentation for the `Digest::` family of modules.
- 💡 **Minimal Dependency**: Does not pull in unnecessary libraries or dependencies.
- 🧪 **Tested Compatibility**: Actively tested with legacy and modern Perl distributions.

## Installation

Install via CPAN:

```bash
cpan Digest::AutoLoader
Or using cpanm:

bash
复制
编辑
cpanm Digest::AutoLoader
Usage
perl
复制
编辑
use Digest::AutoLoader;

my $digest = Digest::AutoLoader->new('MD5');
$digest->add("data");
print $digest->hexdigest;
Supported Backends
Digest::MD5

Digest::SHA

Digest::SHA1

Digest::HMAC

(and any other module conforming to the Digest:: API)

License
This library is free software; you can redistribute it and/or modify it under the same terms as Perl itself.

That means you can use it under either:

the Artistic License 1.0, or

the GNU General Public License (GPL) version 1 or later

See COPYING and LICENSE files for details.
