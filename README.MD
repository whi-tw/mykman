# mykman - ykman for `pass otp`

## Requirements
* [pass](https://www.passwordstore.org/)
* [pass-otp](https://github.com/tadfisher/pass-otp)
* ruby

## Installation

1. Add `mykman` to your `PATH` - most useful if you add it as `ykman` via a symlink
1. Add some otp codes to your `pass` store
1. create `~/.mykman.yml`, as-per mykman-example.yml, as top level `name`:`path/within/pass` pairs.

## Usage

Only `list` and `code` are supported currently. These both output in the same way as their `ykman oath` equivalents:

With stderr output as normal:
```shell
$ ykman oath code some-aws-account
mykman: oath request for some-aws-account
some-aws-account 123456
```
With stderr redirected to /dev/null:
```shell
$ ykman oath code some-aws-account 2>/dev/null
some-aws-account 123456
```
