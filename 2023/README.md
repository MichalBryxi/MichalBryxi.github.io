# Installation

1. Install [LaTeX Workshop][1] code extension

## Windows

1. Install [Tex Live][2]

## Linux
```sh
sudo curl https://gist.githubusercontent.com/rohitrawat/60a04e6ebe4a9ec1203eac3a11d4afc1/raw/fcdfde2ab57e455ba9b37077abf85a81c504a4a9/sources.list -o /etc/apt/sources.list.d/xenial.list
sudo apt install texlive texlive-luatex texlive-bibtex-extra texlive-fonts-extra
```

## macOS
```sh
brew install mactex
brew install font-lato
```

# Build PDF

1. Open the `*.tex` file in vscode
2. Click the "play" icon in the top right corner
3. Open the resulting `*.pdf`

# Build HTML

- There is no build step, PDF will be embeded into the webpage.
- To preview locally, open `index.html` in the root of the repo.

# About

As a base I used [AltaCV Template][3] (v1.6.5, 3 Nov 2022)

## Requirements and Compilation

* AltaCV uses [`fontawesome`][4] and [`academicons`][5]; they're included in both TeX Live 2016 and MikTeX 2.9.
* Loading `academicons` is optional: enable it by adding the `academicons` option to `\documentclass`.
* Can now be compiled with pdflatex, XeLaTeX and LuaLaTeX!
* However if you're using `academicons`, you _must_ use either XeLaTeX or LuaLaTeX. If the doc then compiles but the icons don't show up in the output PDF, try compiling with LuaLaTeX instead.
* The samples here use the [Lato][6] font.

[1]: https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop
[2]: https://www.tug.org/texlive/
[3]: https://www.overleaf.com/latex/templates/altacv-template/trgqjpwnmtgv
[4]: http://www.ctan.org/pkg/fontawesome
[5]: http://www.ctan.org/pkg/academicons
[6]: http://www.latofonts.com/lato-free-fonts/