<p align="center">
  <img src="../../../images/blob/master/TrustNote-Logo-Blue.png" width ="180">
</p>

TrustNote is a Directed Acyclic Graph (DAG) based distributed ledger system and its development platform for the tokenized economy.

<p align="center">
  <img src="../../../images/blob/master/DAG.PNG" width = "800">
</p>

*An illustration of DAG after its main chain is determined. Check out the [TrustNote Whitepaper](https://github.com/trustnote/document) for more information.*

# Development Tools and Samples

This document links to the repositories that are meant to provide development tools for you to use, and examples for you to better understand the features of the [TrustNote network](https://trustnote.org/). The samples are meant to be used with the latest version of the development tools. 

Please feel free to copy and modify the source code herein for your own projects, and please consider sharing your modifications with us, especially if they might benefit other developers using any of the TrustNote technology. See the License for more information.

## headlessRPC: Source-level Development Tool

[TrustNote headlessRPC](https://github.com/trustnotedevelopers/rpc) is not just a light node but also a header-less wallet that provides the RPC services. The wallet has all features of a typical TTT wallet and it supports Remote Procedure Call (RPC). However, due to performance considerations, we do recommend applications to call it locally between processes on the same computer. 

The default port of headlessRPC is 6332. Due to security considerations, if headlessRPC is set up on a server, the RPC port shouldn’t be made accessible to the public.

## Python SDK

[TrustNote Python SDK](https://github.com/TrustNoteDevelopers/sdk_python) is suitable for tokenized applications running on servers, PCs, and IoT devices.

#### Samples:

**A Simple Voting System** - https://github.com/TrustNoteSamples/VotingSystem

**A Simple Web Wallet** - https://github.com/TrustNoteSamples/web_wallet

**Saving Soil Moisture & Air Temperature** - https://github.com/TrustNoteSamples/temp-humi
  
## JavaScript SDK

[TrustNote JavaScript SDK](https://github.com/TrustNoteDeveloper/jssdk) is a tool specifically designed for web developers to implement tokenized applications. If you know how to use jQuery, then you should be able to use the SDK to develop web applications running on TrustNote. 

#### Samples:

**Pay for Read** - https://github.com/TrustNoteSamples/paid_reading

## Rust SDK

Rust is a language for people who value speed and stability. To provide better experiences and more application scenarios, [TrustNote Rust SDK](https://github.com/trustnote/rust-trustnote) currently runs on PC and many X86 based development boards, including:

- Wildfire
- LattePand
- UP Squared
- intel Edison Breakout Board
- Dev-14281 SparkFun

# Questions? Need Help? Found a bug?

If you've got questions about setup, deploying, special feature implementation in your fork, or just want to chat with the developer, please feel free to start a thread in our [Reddit community!](https://www.reddit.com/r/trustnotedev/)
Found a bug with TrustNote? Go ahead and submit an issue. And, of course, feel free to submit pull requests with bug fixes or changes to the dev branch.

# Credits

TrustNote is largely based on Byteball’s source code but also inspired by many other open source projects such as Bitcoin, DASH, IOTA, and Hyperledger Fabric. We are proud to be a donor of Byteball and we hope we can support more innovative open source blockchain projects in the future.
