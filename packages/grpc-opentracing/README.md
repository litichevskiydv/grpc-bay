# grpc-opentracing

[![npm version](https://badge.fury.io/js/grpc-opentracing.svg)](https://www.npmjs.com/package/grpc-opentracing)
[![npm downloads](https://img.shields.io/npm/dt/grpc-opentracing.svg)](https://www.npmjs.com/package/grpc-opentracing)

Interceptors for client and server to track calls through opentracing

# Install

`npm i grpc-opentracing`

# Usage

```javascript
const { clientInterceptor, serverInterceptor } = require("grpc-opentracing");

/*...*/

const server = new GrpcHostBuilder()
  /*...*/
  .addInterceptor(serverInterceptor)
  /*...*/
  .bind(grpcBind)
  .build();

/*...*/
const client = new ServerClient(grpcBind, grpc.credentials.createInsecure(), { interceptors: [clientInterceptor] });
```
