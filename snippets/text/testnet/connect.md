The Moonbase Alpha RPC and WSS endpoints hosted by PureStake are for development purposes only and are not meant to be used in production applications. The following are alternative endpoint providers:

- [OnFinality](https://onfinality.io/)
  - HTTP: `https://moonbeam-alpha.api.onfinality.io/public`
  - WebSocket: `wss://moonbeam-alpha.api.onfinality.io/public-ws`
- [Elara](https://elara.patract.io/)
  - WebSocket: `wss://moonbase.moonbeam.elara.patract.io`

### HTTPS DNS

To connect to Moonbase Alpha via HTTPS, simply point your provider to the following RPC DNS (or one of the alternative endpoints listed above):

```
https://rpc.testnet.moonbeam.network
```

For the web3.js library, you can create a local Web3 instance and set the provider to connect to Moonbase Alpha (both HTTP and WS are supported):

```js
const Web3 = require('web3'); //Load Web3 library
.
.
.
//Create local Web3 instance - set Moonbase Alpha as provider
const web3 = new Web3('https://rpc.testnet.moonbeam.network'); 
```
For the ethers.js library, define the provider by using `ethers.providers.StaticJsonRpcProvider(providerURL, {object})` and setting the provider URL to Moonbase Alpha:

```js
const ethers = require('ethers');


const providerURL = 'https://rpc.testnet.moonbeam.network';
// Define Provider
const provider = new ethers.providers.StaticJsonRpcProvider(providerURL, {
    chainId: 1287,
    name: 'moonbase-alphanet'
});
```

Any Ethereum wallet should be able to generate a valid address for Moonbeam (for example, [MetaMask](https://metamask.io/)).

### WSS DNS

For WebSocket connections, you can use the following DNS:

```
wss://wss.testnet.moonbeam.network
```

### Chain ID

For the Moonbase Alpha TestNet the chain ID is: `1287`.

### Relay Chain

To connect to the Moonbase Alpha relay chain, managed by PureStake, you can use the following WS Endpoint (or one of the alternative endpoints listed above):

```
wss://wss-relay.testnet.moonbeam.network
```