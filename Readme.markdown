# Göktuğ’s Customised Iosevka Fonts

Iosevka variants that

- avoid confusion for symbols like `1, l, I, q, g, O, 0`;
- avoid useless ligatures like `st` because they are fucking dreadful.

Based on v27.3.5.

## Variants

- **Iosevka Cadadrish Sans**: non-serifed
- **Iosevka Cadadrish Sans Textured**: non-serifed variant except with
  the experimental texture control feature enabled

## Build & install

### Get it prebuild from Github

I use Github Actions to auto-build Iosevka Cadadrish. See the releases
page for binary releases.

*The build script YAML thingy is based on [@mjec’s setup][mjec]. Many
thanks!*

[mjec]: https://github.com/mjec/iosevka/blob/main/.github/workflows/release.yml

### Manual build and installation

**BEWARE**: Iosevka builds take about a million years on average!

Clone with depth 1 because the repository is HUGE:

    $ git clone --depth 1 https://github.com/be5invis/Iosevka
    $ cd Iosevka
    $ git checkout v27.3.5
    $ cp $OLDPWD/iosevka-cadadrish.toml private-build-plans.toml

Install a recent version of Node.js, probably using a binary release
because they cut new major releases like a chef dices an onion.

With my own config, it should suffice to extract the binary release to
`~/local/node-...` and then run `$ . ~/.profile`. Otherwise, make sure
to have the `bin/` folder in the `PATH` environment variable.

There are other ways to acquire a recent enough Node.js, but for just
this task, they are an overkill.

Then, build:

    $ sudo apt install ttfautohint
    $ npm install
    $ npm run build -- contents::iosevka-cadadrish-sans
    $ npm run build -- contents::iosevka-cadadrish-sans-texture
    $ cp dist/**/*/*.ttf $HOME/.fonts

If build is consuming too much memory, try with the environment
variable `NODE_OPTIONS="--max-old-space-size=4096"`.

## TODO

- [ ] Perhaps add the Iosevka repo as a submodule?

# Licence for this repo

This project is licenced under the 3-Clause BSD Licence (a.k.a. the
New BSD Licence).

See [LICENCE](./LICENCE) for full text.

# Licence info for Iosevka

Copyright 2015-2021, Renzhi Li (aka. Belleve Invis, belleve@typeof.net)

This Font Software is licensed under the SIL Open Font License, Version 1.1.

For more info, see https://github.com/be5invis/Iosevka/blob/master/LICENSE.md

Original repository URL: https://github.com/be5invis/iosevka
