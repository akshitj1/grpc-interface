# Api contracts for Dealshare Microservices

This is a central library for all Api contracts between microservices.

* The contracts are defined in `protobuf` format. 
* This library can be imported by services and clients for communicating
in `gRPC` protocol. 
* Server interface and client stubs will be auto generated with Models.
* This library is pushed to remote `AWS CodeArtifact`, so that other services can import this just like any other maven repository. [ref.](https://docs.aws.amazon.com/codeartifact/latest/ug/maven-gradle.html)

## Publish library

### locally

In development phase:
```shell
./gradlew publishToMavenLocal
```

Demo Server implementing contract: [grpc-server](https://bitbucket.org/merabolabs/grpc-server/src/master/)