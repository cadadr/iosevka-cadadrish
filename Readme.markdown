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

Clone with depth 1 because the repository is HUGE:

    $ git clone --depth 1 https://github.com/be5invis/Iosevka
    $ cd Iosevka
    $ git checkout v27.3.5
    $ cp $OLDPWD/iosevka-cadadrish.toml private-build-plans.toml

Install a recent version of Node.js, probably using a binary release
because they cut new major releases like a chef dices an onion.

With my own config, it should suffice to extract the binary release to
`~/local/node-...` and then run `$ . ~/.profile`.

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
