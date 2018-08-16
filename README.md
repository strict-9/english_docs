# TrustNote Development Documentation (english)

## Introduction

> TrustNote is a DAG public chain with fast transaction rates and low transaction costs.

![](developers.png)

## Development

### Source-level development tools headlessRPC

headlessRPC is a light node that provides an interfaceless wallet for RPC services. The wallet has all the features of the wallet and can be called remotely, but remote calls are not recommended. It is recommended that the developer call it locally. If it is set up on the server, the RPC port is recommended not to be open to the public.

The headlessRPC default port is 633

### sdk

* python

   For servers, PCs, and IoT devices
  
* js

   For the wallet, the developer builds the H5 page, calls the wallet through jssdk, and completes the functions of reprinting and querying.
  
* rust

   PC and development board for x86 architecture.
