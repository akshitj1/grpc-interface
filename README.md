# Api contracts for gRpc Microservices

Part of blog: [Calling microservice as simple as calling function: gRPC](https://medium.com/@akshit.jain/calling-microservice-as-simple-as-calling-function-grpc-7bec48c2342f)

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

### remote code artifactory

```shell
export CODEARTIFACT_AUTH_TOKEN=`\
  aws codeartifact get-authorization-token \
  --domain akshit \
  --output text`


./gradlew publish
```