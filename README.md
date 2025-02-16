# gRPC Spec Proto

Protocol Buffer extension to specify gRPC Service specification.

Works along with [proto-coverage-reporter](https://www.npmjs.com/package/proto-coverage-reporter).

```proto
syntax = "proto3";

package tutorial;

import "ka_nabellinc/grpc_spec/extension.proto";

service HelloService {
  rpc Greet(GreetRequest) returns (GreetResponse) {
    option (ka_nabellinc.grpc_spec.spec) = {
      status_codes: ["OK", "INVALID_ARGUMENTS", "ALREADY_EXISTS", "PERMISSION_DENIED"]
    };
  }
}
```
