# es-sequence

Node.js module for Elasticsearch that provides sequences of auto-incrementing integers that can be used for document ids.

Inspired by the Perl library [ElasticSearchX-Sequence](https://github.com/clintongormley/ElasticSearchX-Sequence) by borrowing its [approach](http://blogs.perl.org/users/clinton_gormley/2011/10/elasticsearchsequence---a-blazing-fast-ticket-server.html).

[![Build Status](https://travis-ci.org/analog-nico/es-sequence.svg?branch=master)](https://travis-ci.org/analog-nico/es-sequence)

## Installation

This module is installed via npm:

``` bash
$ npm install es-sequence
```

[![NPM Stats](https://nodei.co/npm/es-sequence.png?downloads=true)](https://npmjs.org/package/es-sequence)

## Usage

``` js
var sequence = require('es-sequence');
var elasticsearch = require('elasticsearch');

sequence.init(elasticsearch.Client(), function () {

  sequence.get('userid', function (id) {
    // Use id
  });

});
```
