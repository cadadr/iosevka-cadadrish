# Göktuğ’s Customised Iosevka Fonts

Iosevka variants that

- avoid confusion for symbols like `1, l, I, q, g, O, 0`;
- avoid useless ligatures like `st` because they are fucking dreadful.

## Build & install

Clone with depth 1 because the repository is HUGE. Using my script `git-clonex`:

    $ git clonex --extra '--depth 1' -t -y https://github.com/be5invis/Iosevka
    $ cd <paste clipboard here>

Or just:

    $ cd /tmp
    $ git cone --depth 1 https://github.com/be5invis/Iosevka
    $ cd Iosevka

Then, build:

    $ npm install
    $ npm run build -- contents::iosevka-cadadrish-slap
    $ npm run build -- contents::iosevka-cadadrish-sans
    $ cp dist/**/*/*.ttf $HOME/.fonts

