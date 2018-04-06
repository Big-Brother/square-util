# square-util

[![npm version](https://img.shields.io/npm/v/square-util.svg)](https://www.npmjs.com/package/square-util)
[![Build Status](https://travis-ci.org/dashpay/square-util.svg?branch=master)](https://travis-ci.org/dashpay/square-util)
[![Dependency Status](https://david-dm.org/dashpay/square-util.svg)](https://david-dm.org/dashpay/square-util)

**Utility functions for Square hashes and targets**

## Usage

`npm install square-util`

### Methods

#### `toHash(hex)`

Takes a hex string that contains a Square hash as input, and returns a Square-protocol-friendly little-endian Buffer. Throws an error if the hex string is not of length 64 (representing a 256-bit hash).

#### `compressTarget(target)`

Converts the difficulty target `target` to its compact representation (used in the "bits" field in block headers). `target` should be a `Buffer` (little-endian, the zeroes should be at the end). Returns a `number`.

#### `expandTarget(bits)`

Converts the compressed target integer `bits` to its target hash representation. Returns a `Buffer`.
