# TrustNote Development Documentation (Chinese)

## Introduction

> TrustNote is a DAG public chain with fast transaction rates and low transaction costs.

![](developers.png)

## Development

### Source-level development tools headlessRPC

headlessRPC is a light node that provides an interfaceless wallet for RPC services. The wallet has all the features of the wallet and can be called remotely, but remote calls are not recommended. It is recommended that the developer call it locally. If it is set up on the server, the RPC port is recommended not to be open to the public.

The headlessRPC default port is 633

### sdk

* python

  Used for servers, PCs, and IoT devices.
  
  Examples of development using pythonSDK are:
  
  Voting system: https://github.com/TrustNoteSamples/VotingSystem
  
  Web local wallet: https://github.com/TrustNoteSamples/web_wallet
  
  Flowerpot soil condition chain: https://github.com/TrustNoteSamples/temp-humi
  
* js

  Applicable to the universal wallet, the developer only needs to build the H5 page, complete the reprint through the jssdk call wallet, and process the business logic after the payment is successful through the callback function. Can be widely used to develop a variety of paid applications.
  
  Jssdk example: paid reading
  
  https://github.com/TrustNoteSamples/paid_reading
  
* rust

  PC and development board for x86 architecture (IoT motherboard with x86 architecture).
  
  Currently supported x86 development boards are:
  Wildfire
  2. LattePand
  3. UP Squared
  4. intel Edison Breakout Board
  5. Dev-14281 SparkFun
  n.
