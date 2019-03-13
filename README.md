`ytools` is a set of simple tools to interact with youtube via the terminal.

# Usage
```console
$ ytools-search Black Mambo
 1: Glass Animals - Black Mambo (Lyric Video)
 2: Glass Animals - Black Mambo
 3: Madrugada-Black Mambo
...
$ ytools-info 2
Glass Animals - Black Mambo
14.643.046 Views  ▲ 81.526  ▼ 1.626  Published on 17 Feb 2015

Our new record “How To Be a Human Being” featuring “Youth” and “Life Itself is out now. Buy it and stream it and watch it and take it on a date now: http://po.st/HTBAHBiTunesYT / Listen on Spotify: http://po.st/ListenGlassAnimalsYT / Order from our store: http://po.st/HTBAHBStoreYT
...
$ mpv $(ytools-pick 2)
Playing: https://www.youtube.com/watch?v=H7bqZIpC3Pg
...
$ # Without an argument the comments of the last picked video are shown:
$ ytools-comments
=== Comment #1: ===
If you're here then you have good taste in music... ;)

=== Comment #2: ===
Atyphical
...
$ ytools-recommend
 1: Glass Animals - Cane Shuga
 2: Black Coast - TRNDSTTR (Lucian Remix)
 3: Glass Animals - Season 2 Episode 3 (Official Video)
...
```

# Installation
Right now you have to build `ytools` yourself. All you need to get
started is go.

1. Go to your go workspace source directory (default ist `$HOME/go/src`).
2. `mkdir -p github.com/codesoap/ && cd github.com/codesoap/`
3. `git clone https://github.com/codesoap/ytools.git && cd ytools/`
4. `go get ./...` to install dependencies (`golang.org/x/net/html`)
5. `make all` will build all binaries, you will find them in `bin/`
6. `make install` to install the binaries to `/usr/local/`

To uninstall ytools call `make uninstall`.
