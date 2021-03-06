# benfordslaw

[![Build Status](https://cloud.drone.io/api/badges/CMiksche/benfordslaw/status.svg)](https://cloud.drone.io/CMiksche/benfordslaw)
[![npm version](https://badge.fury.io/js/benfordslaw.svg)](https://badge.fury.io/js/benfordslaw)
![npm](https://img.shields.io/npm/dm/benfordslaw)
![Coverage Branches](./coverage/badge-branches.png)
![Coverage Lines](./coverage/badge-lines.png)
![Coverage Functions](./coverage/badge-functions.png)
![Coverage Statements](./coverage/badge-statements.png)

Check if a number array confirms to the Benford's Law

Heavily inspired by https://github.com/target/huntlib

## Install

    npm i benfordslaw

## Usage

Look at the tests for good examples.

E.g.:

````typescript
import { BenfordsLaw } from 'benfordslaw';

const numbers = [1,2,3,4,5,6,7,8,9];
const benfords = new BenfordsLaw(numbers);

const chiSquared = benfords.getChiSquared();
// chiSquared = 0.40105320411553363
const probability = benfords.getProbability()?.toFixed(1);
// probability = 1.0
````

The ChiSquared result is a float and describes how well Benford's Law was matched. Lower is better.

The Probability describes how relevant ChiSquared is. It should be >= 0.9

getDist() returns the distribution of the numbers.

## Why TypeScript

With Types TypeScript adds a extra layer of security. I also use mainly TypeScript projects with this project so TypeScript just makes sense.
And TS also compiles to JavaScript Code so JS projects also can use it. 

## General Information

License: MIT

Author: Christoph Daniel Miksche

## See also

* https://blog.m5e.de/post/benchmarking-go-crystal-python-and-js/ Benchmarking Benford's Law in different Programming Languages
* https://github.com/CMiksche/benford A Go Package implementation of this benford's law check
* https://github.com/CMiksche/benfordslaw.cr A Crystal implementation of this benford's law check
