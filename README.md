# rbenv-installer

Install [rbenv/rbenv](https://github.com/rbenv/rbenv) +
[rbenv-build/ruby-build](https://github.com/rbenv/ruby-build) (and
other plugins), updating all of them when you want to!

## Installation

It's the standard way: installs `rbenv` in $HOME/.rbenv (default
$RBENV_ROOT value).

```shell
curl -L https://raw.githubusercontent.com/madumlao/rbenv-installer/master/bin/rbenv-installer \
    | bash
```

The script will then instruct you to edit your shell initialization files.

### Optional: Installation in other directory (i.e. system-wide)

If you prefer to install `rbenv` in other directory (i.e
`$HOME/myrbenv`), or perhaps system-wide (i.e. `/usr/local/bin/rbenv`),
it's easy: just set $RBENV_ROOT before the installer command:

```shell
# $HOME/myrbenv
curl -L https://raw.githubusercontent.com/madumlao/rbenv-installer/master/bin/rbenv-installer \
    | RBENV_ROOT=$HOME/myrbenv bash
```

```shell
# /usr/local/bin/rbenv
curl -L https://raw.githubusercontent.com/madumlao/rbenv-installer/master/bin/rbenv-installer \
    | RBENV_ROOT=/usr/local/bin/rbenv bash
```

> Note: depends on the path, you will need superuser (sudo)
permission. Feel free to ask if you need some help!

## Plugins installed by default:

- [rbenv/ruby-build](https://github.com/rbenv/ruby-build): allows `rbenv install`
- [rbenv/rbenv-vars](https://github.com/rbenv/rbenv-vars): allows per-project `.rbenv-vars` files
- [tpope/rbenv-aliases](https://github.com/tpope/rbenv-aliases): provides aliases for ruby versions
- [madumlao/rbenv-binstubs](https://github.com/madumlao/rbenv-binstubs): allows per-project binstubs

## Uninstallation

```shell
rm -rf $(rbenv root)
```

<hr>

Inspired by [phpenv-installer](https://github.com/rogeriopradoj/phpenv-installer) which was ironically inspired by a defunct version of [rbenv-installer](https://github.com/fesplugas/rbenv-installer) and [pyenv-installer](https://github.com/yyuu/pyenv-installer)
