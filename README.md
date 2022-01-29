# Casper C++ SDK
Casper C++ SDK provides an interface to establish a connection between the Casper Blockchain and a client. Currently, the SDK is compatible with Linux systems.

## Dependencies
1. [CMake Version 3.0.0 or newer](https://cmake.org).


## Build

### Debug
    cmake -DCMAKE_BUILD_TYPE=Debug .
    make all

### Release
    cmake -DCMAKE_BUILD_TYPE=Release .
    make all

## Test
    cmake -DCMAKE_BUILD_TYPE=Debug .
    make all
    make test

## Run Example
    cmake -DCMAKE_BUILD_TYPE=Debug .
    make all
    ./examples/HelloSDK

## Install
    cmake -DCMAKE_BUILD_TYPE=Release .
    make all
    sudo make install

---
**NOTE**

Change the CASPER_TEST_ADDRESS value in the CasperClient.h with an RPC Server address to run the examples and the tests.

---
## How to use
    1. Include the header file to the application file.
        #include "CasperClient.h"
    2. Link the installed SDK to the application. A CMake example is given below.
        add_executable(ApplicationName main.cpp)
        target_link_libraries(ApplicationName PUBLIC CasperSDK)

## External Libraries
1. https://github.com/nlohmann/json
2. https://github.com/jsonrpcx/json-rpc-cxx
3. https://github.com/yhirose/cpp-httplib

## TODO
0. MacOS and Windows support
1. The following RPC methods will be fully implemented in the C++ SDK
    * infoGetDeploy
    * infoGetStatus
    * chainGetBlockTransfers
    * chainGetBlock
    * chainGetEraInfoBySwitchBlock
    * stateGetItem
    * stateGetDictionaryItem
    * stateGetBalance
    * stateGetAuctionInfo

2. Documentation
3. C++ version of CLType primitives
4. C++ version for Casper Domain Specific Objects
5. Serialization of Casper Domain Specific Objects
6. ED25519/SECP256K1 key pairs  Wrappers
7. PutDeploy RPC call implemented
8. Refactoring C++ SDK calls to return Casper Domain Specific Objects
