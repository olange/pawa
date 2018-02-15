# Contributing

## Outline

* [Prerequisites](#prerequisites)
* [Setup](#setup)

## Prerequisites

* Git client or command-line – for instance, install [GitHub Desktop](https://desktop.github.com)
* Coding editor for instance [Visual Studio Code](https://code.visualstudio.com) or [Atom](https://atom.io)
* [NodeJS](https://nodejs.org/en/) version 8, or more recent – NodeJS is a JavaScript runtime built on Chrome's V8 engine.

## Setup

### Polymer and Bower

Open a terminal, install the [Polymer 2.0 Command-line interface](https://www.polymer-project.org/2.0/start/install-2-0) (CLI) and the [Bower](https://bower.io) package manager:

```bash
npm install -g polymer-cli
npm install -g bower
```

### Download the sources and client dependencies

```bash
git clone git@github.com:olange/pawa.git
cd pawa/
cd client/
bower install
```

### Download the Neo4j database server

Download the [Neo4j Community Server](https://neo4j.com/download/other-releases/#releases) – version 3.3 or more recent – and install it to the [`server/db/`](../server/db/) subfolder.

For instance, assuming you downloaded the Mac/Linux archive to your `~/Downloads` folder:

```bash
cd server/
tar zxvf ~/Downloads/neo4j-community-3.3.3-unix.tar.gz -C db
```

### Run the client app

```bash
cd client/
polymer serve
```

### Run the Neo4j database server

Open another terminal window and navigate to the project folder:

```bash
cd pawa/server/db/
neo4j-community-‹version›/bin/neo4j console
```

And you should get an output along the lines:

```bash
Active database: graph.db
Directories in use:
  home:         /Users/oliv/Sources/pawa/server/db/neo4j-community-3.3.3
  config:       /Users/oliv/Sources/pawa/server/db/neo4j-community-3.3.3/conf
  logs:         /Users/oliv/Sources/pawa/server/db/neo4j-community-3.3.3/logs
  plugins:      /Users/oliv/Sources/pawa/server/db/neo4j-community-3.3.3/plugins
  import:       /Users/oliv/Sources/pawa/server/db/neo4j-community-3.3.3/import
  data:         /Users/oliv/Sources/pawa/server/db/neo4j-community-3.3.3/data
  certificates: /Users/oliv/Sources/pawa/server/db/neo4j-community-3.3.3/certificates
  run:          /Users/oliv/Sources/pawa/server/db/neo4j-community-3.3.3/run
Starting Neo4j.
2018-02-15 16:56:23.024+0000 INFO  ======== Neo4j 3.3.3 ========
2018-02-15 16:56:23.060+0000 INFO  Starting...
2018-02-15 16:56:25.446+0000 INFO  Bolt enabled on 127.0.0.1:7687.
2018-02-15 16:56:28.327+0000 INFO  Started.
2018-02-15 16:56:29.291+0000 INFO  Remote interface available at http://localhost:7474/
```

Open a browser window and try to login to [`http://localhost:7474`](http://localhost:7474) with user `neo4j` and password `neo4j`, then change that initial password to one you'll remember easily while developing.