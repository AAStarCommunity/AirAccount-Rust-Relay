# AirAccount-Rust-Relay
A basic relay to manage your private key and account life cycle with API and passkey verification.
This repo only responsible for the basic manmagement, for security features, check Tauri framework with TEE(https://github.com/AAStarCommunity/COS72-Tauri).
This repo will be part of the Tauri Node framework(migrate to it).

## Flow
1. Get request with finger passkey encryption and verify it from client app.
2. If passed, finish the API invoking method
3. Response with the node signature.

## Services
### Verify
Verify Email
Verify EOA
### Binding
Bind Finger print passkey in the first time or more with exist account
### Create
Create a new contract account record with private key
### _Create
The same, but for internal call in the first binding in specific chainId

### SSOLogin(no Zk for now)
provide a email to get a ens and contract address.
will get a ZK version later: provide a ZK Proof（get from local ZK SDK) to SSO, if verified, get a contract address and ens.
