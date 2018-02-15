# Contributing

## Outline

* [Prerequisites](#Prerequisites)
* [Setup](#Setup)

## Prerequisites

* Git client or command-line – for instance, install [GitHub Desktop](https://desktop.github.com)
* Coding editor for instance [Visual Studio Code](https://code.visualstudio.com) or [Atom](https://atom.io)
* [NodeJS](https://nodejs.org/en/) version 8, or more recent – NodeJS is a JavaScript runtime built on Chrome's V8 engine.

## Setup

### Polymer and Bower

Open a terminal, install the [Polymer 2.0 Command-line interface](https://www.polymer-project.org/2.0/start/install-2-0) (CLI) and the [Bower](https://bower.io) package manager:

```
npm install -g polymer-cli
npm install -g bower
```

### Get the sources

```
git clone git@github.com:olange/pawa.git
cd pawa/
```

### Setup the client app

```
cd client/
bower install
```

### Run the client app

```
cd client/
polymer serve
```