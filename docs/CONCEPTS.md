# Concepts

## Overview

The animation is built with the Phaser Game Engine, as an application running in a web browser, using Polymer Web Components and an immutable Redux datastore.

On the back-end, the app uses a graph database, Neo4j, to calculate shortests paths of the boats, depending on the current wind flow field.

And if time permits, the back-end will fetch meteorologic data from remote servers and feed the database from the live data.

## Data model

* _Front-end data model_ — with _boats_, _weather stations_, _ports_, _lake contour_, _shortest paths_ and _wind flow field_.
* _Back-end data model_ – with wind flow field and possible paths among the cells of the flow field, weighted by the wind speed.
* as well as a _geographic mesh_ euclidian coordinate system, used in both the front-end and back-end data models, to represent locations of the various entities.

## Animation techniques

* Perlin Noise and Simplex Noise
* Path following
* Flow field

## Core libraries

### Datastore

* [Immutable JS API](https://facebook.github.io/immutable-js/docs/#/) – we used mostly [Records](https://facebook.github.io/immutable-js/docs/#/Record), [Maps](https://facebook.github.io/immutable-js/docs/#/Map), [Lists](https://facebook.github.io/immutable-js/docs/#/List) and [Sets](https://facebook.github.io/immutable-js/docs/#/Set)
* [Redux API](https://redux.js.org)

### Phaser Game Engine

Version 3 of Phaser was used, which was published these days (version 3.1 released today, on 19.02). Its documentation is mature, although currently in a state of flux.

Reference documents we suggest to refer to:

* [Phaser 3 API](https://phaser.io/phaser3/api/) _the official Phaser 3 API documentation_
* [Phaser 3 Source code](https://github.com/photonstorm/phaser/tree/master/src) _the ultimate reference_
* [Phaser 3 Examples](https://github.com/photonstorm/phaser3-examples) _a repository with a collection of Phaser 3 code snippets and examples – also available [online](https://labs.phaser.io)_.

Look at every one of the [Systems](https://phaser.io/phaser3/api/systems), especially the [Scene Manager](https://phaser.io/phaser3/api/scene-manager) and [Boot process](https://phaser.io/phaser3/api/boot) system parts, in the API documentation, as a good starting point.

Later, have a look at the [Actions](https://phaser.io/phaser3/api/actions), [Game Objects](https://phaser.io/phaser3/api/gameobjects), [Geometry Objects](https://phaser.io/phaser3/api/geometry) and [Math functions](https://phaser.io/phaser3/api/math) to get a grip on everything you might use to build a game.

:warning: Beware! Many sample code and question/answers on StackOverflow and the Internet still refer to Phaser 2, as it is quite popular. Keep it in mind when reading sample code and check the Phaser 3 API docs for eventual changes.