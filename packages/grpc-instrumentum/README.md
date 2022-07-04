# grpc-instrumentum

[![npm version](https://badge.fury.io/js/grpc-instrumentum.svg)](https://www.npmjs.com/package/grpc-instrumentum)
[![npm downloads](https://img.shields.io/npm/dt/grpc-instrumentum.svg)](https://www.npmjs.com/package/grpc-instrumentum)

A set of tools to simplify working with protoc

# Install

`npm i grpc-instrumentum`

# Usage

## grpc-gen-js

```
$ grpc-gen-js --js_out=import_style=commonjs,binary:./tests/generated/client --grpc_out=./tests/generated/client -I ./tests/protos greeter.proto
```

## grpc-gen-ts

```
$ grpc-gen-ts --ts_out=./tests/generated/client -I ./tests/protos greeter.proto
```

## grpc-gen-ts

```
grpc-gen-client --help
grpc-gen-client.js [options] <protoFile>

Produces clients for all services from given proto file

Options:
  --help         Show help               [boolean]
  --version      Show version number     [boolean]
  -i, --include  Include directory         [array]
  -o, --out      Output directory         [string] [default: Currnt working directory]
```

```
$ grpc-gen-client --out ./tests/generated/client --include ./tests/protos/ greeter.proto
```
