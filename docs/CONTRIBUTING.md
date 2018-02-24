# Contributing

## Outline

* [Prerequisites](#prerequisites)
* [Setup](#setup)

## Prerequisites

* [Git](https://git-scm.com) client or command-line – for instance, install [GitHub Desktop](https://desktop.github.com)
* A coding editor, for instance [Visual Studio Code](https://code.visualstudio.com), [Atom](https://atom.io), …
* [NodeJS](https://nodejs.org/en/) version 8, or more recent – NodeJS is a JavaScript runtime built on Chrome's V8 engine
* [Java SDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) version 8, which is needed to run the Neo4j database server – note the Java Runtime Environment (JRE) is not enough, and that Java version 9 is not supported yet by Neo4j 3.3!

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
npm install
```

### Download the Neo4j database server

Download the [Neo4j Community Server](https://neo4j.com/download/other-releases/#releases) – version 3.3 or more recent – and install it to the [`server/db/`](../server/db/) subfolder.

For instance, assuming you downloaded the Mac/Linux archive to your `~/Downloads` folder:

```bash
cd server/
tar zxvf ~/Downloads/neo4j-community-3.3.3-unix.tar.gz -C db
```

Alternatively, for a Windows installation, download the ZIP archive (32-bit or 64-bit, depending on your computer – probably 64-bit for a recent machine) and unpack it to the `server/db/' folder of the project.

See also: [Installation instructions](https://neo4j.com/docs/operations-manual/current/installation/) from Neo4j.

### Run the client app

```bash
npm run start-app
```

You should see an output along the following lines:

```bash
> pawa@1.0.0 start-app …/pawa
> cd client && polymer serve

info:    Files in this directory are available under the following URLs
      applications: http://127.0.0.1:8081
      reusable components: http://127.0.0.1:8081/components/client/
```

### Run the Neo4j database server

Open another terminal window and navigate to the project folder:

```bash
npm run start-db
```

And you should see an output along the lines:

```bash
> pawa@1.0.0 start-db …/pawa
> run-script-os

…

Active database: graph.db
Directories in use:
  home:         …/pawa/server/db/neo4j-community-3.3.3
  config:       …/pawa/server/db/neo4j-community-3.3.3/conf
  logs:         …/pawa/server/db/neo4j-community-3.3.3/logs
  plugins:      …/pawa/server/db/neo4j-community-3.3.3/plugins
  import:       …/pawa/server/db/neo4j-community-3.3.3/import
  data:         …/pawa/server/db/neo4j-community-3.3.3/data
  certificates: …/pawa/server/db/neo4j-community-3.3.3/certificates
  run:          …/pawa/server/db/neo4j-community-3.3.3/run
Starting Neo4j.
2018-02-15 16:56:23.024+0000 INFO  ======== Neo4j 3.3.3 ========
2018-02-15 16:56:23.060+0000 INFO  Starting...
2018-02-15 16:56:25.446+0000 INFO  Bolt enabled on 127.0.0.1:7687.
2018-02-15 16:56:28.327+0000 INFO  Started.
2018-02-15 16:56:29.291+0000 INFO  Remote interface available at http://localhost:7474/
```

Open a browser window and try to login to [`http://localhost:7474`](http://localhost:7474) with user `neo4j` and password `neo4j`. Then change that initial password to one you'll remember easily while developing.