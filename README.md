# Tony's sample golang app

Same golang web application for [*The Tao of tmux and Terminal Tricks*](https://leanpub.com/the-tao-of-tmux/read).

## Features

* [`Makefile`](https://en.wikipedia.org/wiki/Makefile) with [file watching functionality from the
  book](https://leanpub.com/the-tao-of-tmux/read#leanpub-auto-file-watching)

  * `make build` - generate game app
  * `make watch_build` - rebuild build application on code file change
  * `make run` - launch server
  * `make watch_run` launch server and restart on file change

    ![screenshot](resources/screenshot.png)
  * `make lint` - [golint](https://github.com/golang/lint) 
  * `make watchlint` relint on file change
  * `make metalint` - [gometalinter](https://github.com/alecthomas/gometalinter) 
  * `make watchmetalint` - gometalinter on file change

* Load project with [tmuxp](https://tmuxp.git-pull.com) via `$ tmuxp load .` in
  the project directory. See [`.tmuxp.yaml`](.tmuxp.yaml)

## Dependencies

- [golang](https://golang.org/)
- [tmuxp](https://tmuxp.git-pull.com)
- [`entr(1)`](http://entrproject.org/)
- [bower](https://bower.io/#install-bower), installed via [npm](https://nodejs.org/en/)

## Installation

Grab project and go dependencies:

```bash
$ go get -u github.com/mmlogin/tot-go-webapp
```

Install CSS dependencies (from project dir):

```bash
$ bower install
```

## Build n' run

```bash
$ make run
```

Then go to http://localhost:8080

## License

MIT.
