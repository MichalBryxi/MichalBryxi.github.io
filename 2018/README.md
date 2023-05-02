# Installation

1. Install [LaTeX Workshop][1] code extension

## Windows

1. Install [Tex Live][2]

## Linux
```sh
sudo curl https://gist.githubusercontent.com/rohitrawat/60a04e6ebe4a9ec1203eac3a11d4afc1/raw/fcdfde2ab57e455ba9b37077abf85a81c504a4a9/sources.list -o /etc/apt/sources.list.d/xenial.list
sudo apt install texlive texlive-luatex texlive-bibtex-extra texlive-fonts-extra pdf2htmlex
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

To (redo) build:
```sh 
pdf2htmlEX 2018/Michal_Bryxi_CV.pdf; mv Michal_Bryxi_CV.html index.html
```

To preview changes:
```sh
python3 -m http.server
```

Go to: [http://0.0.0.0:8000/out/Michal_Bryxi_CV.html](http://0.0.0.0:8000/out/Michal_Bryxi_CV.html)

# AltaCV, yet another LaTeX CV/Résumé class

v1.1.4 (27 July 2018), by LianTze Lim (liantze@gmail.com)

(Thanks to [Nur](https://github.com/nurh) for the name.)

It all started with this:

[<img src="tweet-that-started-this.png" width="500px">]
(https://twitter.com/Leonduck/status/764281546408923136)

Leonardo was talking about a [résumé of Marissa Mayer that Business Insider put together](http://www.businessinsider.my/a-sample-resume-for-marissa-mayer-2016-7/) using [enhancv.com](https://enhancv.com).
I _knew_ I had to do something about it. And so AltaCV was born.

## Samples

This is how the re-created résumé looks like ([view/open on Overleaf](https://www.overleaf.com/read/gtqfpbwncfvp)):

<img src="mmayer.png" alt="Marissa Mayer's résumé, re-created with AltaCV" width="600px">

Though if you're creating your own CV/résumé, you'd probably prefer using the basic template ([view/open on Overleaf](https://www.overleaf.com/read/trgqjpwnmtgv)):

<img src="sample.png" alt="sample barebones AltaCV template" width="600px">


## Requirements and Compilation

* AltaCV uses [`fontawesome`](http://www.ctan.org/pkg/fontawesome) and [`academicons`](http://www.ctan.org/pkg/academicons); they're included in both TeX Live 2016 and MikTeX 2.9.
* Loading `academicons` is optional: enable it by adding the `academicons` option to `\documentclass`.
* Can now be compiled with pdflatex, XeLaTeX and LuaLaTeX!
* However if you're using `academicons`, you _must_ use either XeLaTeX or LuaLaTeX. If the doc then compiles but the icons don't show up in the output PDF, try compiling with LuaLaTeX instead.
* The samples here use the [Lato](http://www.latofonts.com/lato-free-fonts/) font.

[1]: https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop
[2]: https://www.tug.org/texlive/