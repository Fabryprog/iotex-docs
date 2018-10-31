---
id: iotex-client-js
title: iotex-client-js v0.0.7
---

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [TWallet][1]
    -   [Properties][2]
-   [TUnsignedTransfer][3]
    -   [Properties][4]
-   [TUnsignedExecution][5]
    -   [Properties][6]
-   [Accounts][7]
    -   [Parameters][8]
    -   [Examples][9]
    -   [create][10]
    -   [privateKeyToAccount][11]
        -   [Parameters][12]
    -   [add][13]
        -   [Parameters][14]
    -   [signTransfer][15]
        -   [Parameters][16]
    -   [signSmartContract][17]
        -   [Parameters][18]
-   [TContractOpts][19]
    -   [Properties][20]
-   [TMethodsOpts][21]
    -   [Properties][22]
-   [Contract][23]
    -   [Parameters][24]
    -   [methods][25]
    -   [deploy][26]
        -   [Parameters][27]
    -   [prepareMethods][28]
        -   [Parameters][29]
-   [Iotx][30]
    -   [Parameters][31]
    -   [Examples][32]
    -   [sendTransfer][33]
        -   [Parameters][34]
-   [Request][35]
    -   [Properties][36]
-   [Response][37]
    -   [Properties][38]
-   [Provider][39]
    -   [Properties][40]
-   [HttpProvider][41]
    -   [Parameters][42]
    -   [send][43]
        -   [Parameters][44]
-   [TCoinStatistic][45]
    -   [Properties][46]
-   [TBlockGenerator][47]
    -   [Properties][48]
-   [TBlock][49]
    -   [Properties][50]
-   [TTransfer][51]
    -   [Properties][52]
-   [TExecution][53]
    -   [Properties][54]
-   [TLog][55]
    -   [Properties][56]
-   [TReceipt][57]
    -   [Properties][58]
-   [TVote][59]
    -   [Properties][60]
-   [TAddressDetails][61]
    -   [Properties][62]
-   [TCandidate][63]
    -   [Properties][64]
-   [TCandidateMetrics][65]
    -   [Properties][66]
-   [TConsensusMetrics][67]
    -   [Properties][68]
-   [TSendTransferRequest][69]
    -   [Properties][70]
-   [TSendTransferResponse][71]
    -   [Properties][72]
-   [TSendVoteRequest][73]
    -   [Properties][74]
-   [TSendVoteResponse][75]
    -   [Properties][76]
-   [TNode][77]
    -   [Properties][78]
-   [TGetPeersResponse][79]
    -   [Properties][80]
-   [TSendSmartContractResponse][81]
    -   [Properties][82]
-   [RpcMethods][83]
    -   [Parameters][84]
    -   [Examples][85]
    -   [getBlockchainHeight][86]
    -   [getAddressBalance][87]
        -   [Parameters][88]
    -   [getAddressDetails][89]
        -   [Parameters][90]
    -   [getLastTransfersByRange][91]
        -   [Parameters][92]
    -   [getTransferByID][93]
        -   [Parameters][94]
    -   [getTransfersByAddress][95]
        -   [Parameters][96]
    -   [getUnconfirmedTransfersByAddress][97]
        -   [Parameters][98]
    -   [getTransfersByBlockID][99]
        -   [Parameters][100]
    -   [getLastVotesByRange][101]
        -   [Parameters][102]
    -   [getVoteByID][103]
        -   [Parameters][104]
    -   [getVotesByAddress][105]
        -   [Parameters][106]
    -   [getUnconfirmedVotesByAddress][107]
        -   [Parameters][108]
    -   [getVotesByBlockID][109]
        -   [Parameters][110]
    -   [getLastExecutionsByRange][111]
        -   [Parameters][112]
    -   [getExecutionByID][113]
        -   [Parameters][114]
    -   [getExecutionsByAddress][115]
        -   [Parameters][116]
    -   [getUnconfirmedExecutionsByAddress][117]
        -   [Parameters][118]
    -   [getExecutionsByBlockID][119]
        -   [Parameters][120]
    -   [getLastBlocksByRange][121]
        -   [Parameters][122]
    -   [getBlockByID][123]
        -   [Parameters][124]
    -   [getCoinStatistic][125]
    -   [getConsensusMetrics][126]
    -   [getCandidateMetrics][127]
    -   [sendTransfer][128]
        -   [Parameters][129]
    -   [sendVote][130]
        -   [Parameters][131]
    -   [sendSmartContract][132]
        -   [Parameters][133]
    -   [getPeers][134]
    -   [getReceiptByExecutionID][135]
        -   [Parameters][136]
    -   [readExecutionState][137]
        -   [Parameters][138]

## TWallet

TWallet type contains the private key, public key, and raw address.

Type: {privateKey: [string][139], publicKey: [string][139], rawAddress: [string][139]}

### Properties

-   `privateKey` **[string][139]**
-   `publicKey` **[string][139]**
-   `rawAddress` **[string][139]**

## TUnsignedTransfer

TUnsignedTransfer is the type of unsigned transfer to be signed.

Type: {version: [number][140], nonce: [number][140], amount: [number][140], sender: [string][139], recipient: [string][139], payload: [string][139], isCoinbase: [boolean][141], senderPubKey: [string][139], gasLimit: [number][140], gasPrice: [string][139]}

### Properties

-   `version` **[number][140]**
-   `nonce` **[number][140]**
-   `amount` **[number][140]**
-   `sender` **[string][139]**
-   `recipient` **[string][139]**
-   `payload` **[string][139]**
-   `isCoinbase` **[boolean][141]**
-   `senderPubKey` **[string][139]**
-   `gasLimit` **[number][140]**
-   `gasPrice` **[string][139]**

## TUnsignedExecution

UnsignedExecution is the type of the unsigned execution to be signed.

Type: {byteCode: [string][139], nonce: [number][140]?, gasLimit: [number][140], version: [number][140], contract: [string][139]?, amount: [string][139]}

### Properties

-   `byteCode` **[string][139]**
-   `nonce` **[number][140]?**
-   `gasLimit` **[number][140]**
-   `version` **[number][140]**
-   `contract` **[string][139]?**
-   `amount` **[string][139]**

## Accounts

Accounts contains functions to generate Iotex accounts and sign transactions and data.

### Parameters

-   `rpcMethods` **[RpcMethods][142]**

### Examples

```javascript
import {Accounts, HttpProvider} from 'iotex-client-js';
const accounts = new Accounts(new HttpProvider('http://localhost:4004/api/wallet-core/'));
const wallet = await accounts.create();
// => {
//   "publicKey": "...",
//   "privateKey": "...",
//   "rawAddress": "..."
// }


const unlockedWallet = await accounts.add('...iotx private key...');
// => {
//   "publicKey": "...",
//   "privateKey": "...",
//   "rawAddress": "..."
// }
accounts.wallets[unlockedWallet.publicKey];
// => {
//   "publicKey": "...",
//   "privateKey": "...",
//   "rawAddress": "..."
// }
```

### create

create generates a wallet and add it to local wallets.

Returns **[Promise][143]&lt;[TWallet][144]>**

### privateKeyToAccount

privateKeyToAccount gets the whole wallet from private key.

#### Parameters

-   `privateKey` **[string][139]**

Returns **[Promise][143]&lt;[TWallet][144]>**

### add

privateKeyToAccount gets the whole wallet from private key and save it to local wallets.

#### Parameters

-   `privateKey` **[string][139]**

Returns **[Promise][143]&lt;[TWallet][144]>**

### signTransfer

signTransfer signs a transfer with the wallet.

#### Parameters

-   `unsignedTransfer` **[TUnsignedTransfer][145]**
-   `wallet` **[TWallet][144]**

### signSmartContract

signSmartContract signs an execution with the wallet.

#### Parameters

-   `wallet` **[TWallet][144]**
-   `exec` **[TUnsignedExecution][146]**

Returns **any**

## TContractOpts

TContractOpts are the settings to create the contract object with.

Type: {provider: [Provider][147], abi: any, contractAddress: [string][139], rpcMethods: [RpcMethods][142], accounts: [Accounts][148], wallet: {publicKey: [string][139], privateKey: [string][139], rawAddress: [string][139]}}

### Properties

-   `provider` **[Provider][147]**
-   `abi` **any**
-   `contractAddress` **[string][139]**
-   `rpcMethods` **[RpcMethods][142]**
-   `accounts` **[Accounts][148]**
-   `wallet` **{publicKey: [string][139], privateKey: [string][139], rawAddress: [string][139]}**
-   `wallet.publicKey` **[string][139]**
-   `wallet.privateKey` **[string][139]**
-   `wallet.rawAddress` **[string][139]**

## TMethodsOpts

TMethodsOpts are settings to call smart contract methods with.

Type: {contractAddress: [string][139], nonce: [number][140], gasLimit: [number][140], gasPrice: [string][139], version: [number][140], amount: [string][139]}

### Properties

-   `contractAddress` **[string][139]**
-   `nonce` **[number][140]**
-   `gasLimit` **[number][140]**
-   `gasPrice` **[string][139]**
-   `version` **[number][140]**
-   `amount` **[string][139]**

## Contract

Contract makes it easy to interact with smart contracts on the iotex blockchain. When you create a new contract
object you give it the json interface of the respective smart contract and it will auto converts all calls into
low level ABI calls over RPC for you.

This allows you to interact with smart contracts as if they were JavaScript objects.

### Parameters

-   `opts` **[TContractOpts][149]** ContractOpts are the settings to create the contract object with.

### methods

methods are the ABI's methods of the smart contract the user can call.

Type: {}

### deploy

deploy signs an execution and then send it to the iotex blockchain.

#### Parameters

-   `exec` **[TUnsignedExecution][146]**

Returns **[Promise][143]&lt;[TExecution][150]>**

### prepareMethods

prepareMethods prepares calls of smart contract with method options.

#### Parameters

-   `opts` **[TMethodsOpts][151]** are the settings to call methods with.

## Iotx

Iotx is the client to interact with iotex-core and iotex-wallet.

### Parameters

-   `provider` **[Provider][147]** is the network provider/endpoint this client will interact with.

### Examples

```javascript
import {Iotx, HttpProvider} from 'iotex-client-js';

const iotx = new Iotx(new HttpProvider('http://localhost:14004/'));

// create a new wallet which contains a public key, a private key, and a raw address.
const wallet = await iotx.accounts.create();
// => {
//   "publicKey": "...",
//   "privateKey": "...",
//   "rawAddress": "..."
// }

// recover the whole wallet from a single private key
const unlockedWallet = await iotx.accounts.add('...iotx private key...');
// => {
//   "publicKey": "...",
//   "privateKey": "...",
//   "rawAddress": "..."
// }
accounts.wallets[unlockedWallet.publicKey];
// => {
//   "publicKey": "...",
//   "privateKey": "...",
//   "rawAddress": "..."
// }


// send transfer
const receipt = await iotx.sendTransfer({
  amount: '1',
  sender: unlockedWallet.rawAddress,
  senderPubKey: unlockedWallet.publicKey,
  recipient: 'recipientAddress',
  gasPrice: '1',
  gasLimit: 1,
});


// compile and deploy a contract
const solidityFileString = `
pragma solidity ^0.4.0;

contract SimpleStorage {
   uint storedData;

   function set(uint x) public {
       storedData = x;
   }

   function get() public view returns (uint) {
       return storedData;
   }
}
`;
const contractName = ':SimpleStorage';
const output = solc.compile(solidityFileString, 1);
const abi = JSON.parse(output.contracts[contractName].interface);
const provider = new HttpProvider('http://localhost:14004/');
const iotx = new Iotx(provider);
const wallet = await iotx.accounts.add('c5364b1a2d99d127439be22edfd657889981e9ba4d6d18fe8eca489d48485371efcb2400');
const bytecode = output.contracts[contractName].bytecode;
const contract = new iotx.Contract({abi, contractName, wallet});
const exec = await contract.deploy({
   byteCode: bytecode,
   gasLimit: 100000,
   gasPrice: '0',
   version: 1,
   contract: '',
   amount: '1',
 });

const timeout = time => new Promise(resolve => window.setTimeout(resolve, time));
await timeout(5000);

const receipt = await iotx.rpcMethods.getReceiptByExecutionID(exec.ID);

// call methods in the smart contract deployed
await contract
.prepareMethods({
     contractAddress: receipt.contractAddress,
     gasLimit: 100000,
     gasPrice: '0',
     version: 1,
     amount: '0',
   })
.set(666);

const value = await contract
.prepareMethods({
     contractAddress: receipt.contractAddress,
     gasLimit: 100000,
     gasPrice: '0',
     version: 1,
     amount: '0',
   })
.get();
```

### sendTransfer

sendTransfer signs, send, and get receipt of the transfer.

#### Parameters

-   `transfer` **[TUnsignedTransfer][145]** : the transfer to be sent.

Returns **[Promise][143]&lt;[TTransfer][152]>**

## Request

Request is the type of the request sent from the Provider.

Type: {method: [string][139], params: [Array][153]&lt;any>}

### Properties

-   `method` **[string][139]**
-   `params` **[Array][153]&lt;any>**

## Response

Response is the response type received by the Provider.

Type: {result: any, error: {code: [number][140], message: [string][139]}}

### Properties

-   `result` **any**
-   `error` **{code: [number][140], message: [string][139]}**
-   `error.code` **[number][140]**
-   `error.message` **[string][139]**

## Provider

Provider is the network provider interface of iotex backend.

### Properties

-   `send` **function (request: [Request][154]): [Promise][143]&lt;[Response][155]>**

## HttpProvider

Provider is the network provider of iotex backend that is implemented in HTTP.

### Parameters

-   `url` **[string][139]**
-   `timeout` **[number][140]?**

### send

send makes an xhr call to the url.

#### Parameters

-   `request` **[Request][154]**

Returns **[Promise][143]&lt;[Response][155]>**

## TCoinStatistic

TCoinStatistic is the type of stats of the iotx coin.

Type: {height: [number][140], supply: [number][140], transfers: [number][140], votes: [number][140], executions: [number][140], aps: [number][140]}

### Properties

-   `height` **[number][140]**
-   `supply` **[number][140]**
-   `transfers` **[number][140]**
-   `votes` **[number][140]**
-   `executions` **[number][140]**
-   `aps` **[number][140]**

## TBlockGenerator

TBlockGenerator is the type that identifies the generator of the block.

Type: {name: [string][139], address: [string][139]}

### Properties

-   `name` **[string][139]**
-   `address` **[string][139]**

## TBlock

TBlock is the type of the meta data of the block.

Type: {ID: [string][139], height: [number][140], timestamp: [number][140], transfers: [number][140], votes: [number][140], executions: [number][140], generateBy: [TBlockGenerator][156], amount: [number][140], forged: [number][140], size: [number][140]}

### Properties

-   `ID` **[string][139]**
-   `height` **[number][140]**
-   `timestamp` **[number][140]**
-   `transfers` **[number][140]**
-   `votes` **[number][140]**
-   `executions` **[number][140]**
-   `generateBy` **[TBlockGenerator][156]**
-   `amount` **[number][140]**
-   `forged` **[number][140]**
-   `size` **[number][140]**

## TTransfer

TTransfer is the type of the transfer.

Type: {version: [number][140], ID: [string][139], nonce: [number][140], sender: [string][139], recipient: [string][139], amount: [number][140], senderPubKey: [string][139], payload: [string][139], isCoinbase: [boolean][141], fee: [number][140], timestamp: [number][140], blockID: [string][139], isPending: [boolean][141], signature: [string][139]?}

### Properties

-   `version` **[number][140]**
-   `ID` **[string][139]**
-   `nonce` **[number][140]**
-   `sender` **[string][139]**
-   `recipient` **[string][139]**
-   `amount` **[number][140]**
-   `senderPubKey` **[string][139]**
-   `payload` **[string][139]**
-   `isCoinbase` **[boolean][141]**
-   `fee` **[number][140]**
-   `timestamp` **[number][140]**
-   `blockID` **[string][139]**
-   `isPending` **[boolean][141]**
-   `signature` **[string][139]?**

## TExecution

TExecution is the type of the execution to be sent to the iotex blockchain.

Type: {version: [number][140], ID: [string][139], nonce: [number][140], executor: [string][139], contract: [string][139], amount: [string][139], executorPubKey: [string][139], signature: [string][139], gasLimit: [number][140], gasPrice: [string][139], timestamp: [number][140], data: [string][139], blockID: [string][139], isPending: [boolean][141]}

### Properties

-   `version` **[number][140]**
-   `ID` **[string][139]**
-   `nonce` **[number][140]**
-   `executor` **[string][139]**
-   `contract` **[string][139]**
-   `amount` **[string][139]**
-   `executorPubKey` **[string][139]**
-   `signature` **[string][139]**
-   `gasLimit` **[number][140]**
-   `gasPrice` **[string][139]**
-   `timestamp` **[number][140]**
-   `data` **[string][139]**
-   `blockID` **[string][139]**
-   `isPending` **[boolean][141]**

## TLog

TLog is the type of the log in the smart contract log.

Type: {address: [string][139], topics: [Array][153]&lt;[string][139]>, data: [string][139], blockNumber: [number][140], txnHash: [string][139], blockHash: [string][139], index: [number][140]}

### Properties

-   `address` **[string][139]**
-   `topics` **[Array][153]&lt;[string][139]>**
-   `data` **[string][139]**
-   `blockNumber` **[number][140]**
-   `txnHash` **[string][139]**
-   `blockHash` **[string][139]**
-   `index` **[number][140]**

## TReceipt

TReceipt is the type of the receipt.

Type: {returnValue: [string][139], status: [number][140], hash: [string][139], gasConsumed: [number][140], contractAddress: [string][139], logs: [Array][153]&lt;[TLog][157]>}

### Properties

-   `returnValue` **[string][139]**
-   `status` **[number][140]**
-   `hash` **[string][139]**
-   `gasConsumed` **[number][140]**
-   `contractAddress` **[string][139]**
-   `logs` **[Array][153]&lt;[TLog][157]>**

## TVote

TVote is the type of the vote.

Type: {version: [number][140], ID: [string][139], nonce: [number][140], timestamp: [number][140], voter: [string][139], votee: [string][139], voterPubKey: [string][139], signature: [string][139], blockID: [string][139], isPending: [boolean][141]}

### Properties

-   `version` **[number][140]**
-   `ID` **[string][139]**
-   `nonce` **[number][140]**
-   `timestamp` **[number][140]**
-   `voter` **[string][139]**
-   `votee` **[string][139]**
-   `voterPubKey` **[string][139]**
-   `signature` **[string][139]**
-   `blockID` **[string][139]**
-   `isPending` **[boolean][141]**

## TAddressDetails

TAddressDetails is the type of the address' account detail.

Type: {address: [string][139], totalBalance: [number][140], nonce: [number][140], pendingNonce: [number][140], isCandidate: [boolean][141]}

### Properties

-   `address` **[string][139]**
-   `totalBalance` **[number][140]**
-   `nonce` **[number][140]**
-   `pendingNonce` **[number][140]**
-   `isCandidate` **[boolean][141]**

## TCandidate

TCandidate is the type of the candidate.

Type: {address: [string][139], totalVote: [number][140], creationHeight: [number][140], lastUpdateHeight: [number][140], isDelegate: [boolean][141], isProducer: [boolean][141]}

### Properties

-   `address` **[string][139]**
-   `totalVote` **[number][140]**
-   `creationHeight` **[number][140]**
-   `lastUpdateHeight` **[number][140]**
-   `isDelegate` **[boolean][141]**
-   `isProducer` **[boolean][141]**

## TCandidateMetrics

TCandidateMetrics is the type of the candidate metrics.

Type: {candidates: [Array][153]&lt;[TCandidate][158]>, latestEpoch: [number][140], latestHeight: [number][140]}

### Properties

-   `candidates` **[Array][153]&lt;[TCandidate][158]>**
-   `latestEpoch` **[number][140]**
-   `latestHeight` **[number][140]**

## TConsensusMetrics

TConsensusMetrics is the type of the consensus metrics.

Type: {latestEpoch: [number][140], latestDelegates: [Array][153]&lt;[string][139]>, latestBlockProducer: [string][139], candidates: [Array][153]&lt;[string][139]>}

### Properties

-   `latestEpoch` **[number][140]**
-   `latestDelegates` **[Array][153]&lt;[string][139]>**
-   `latestBlockProducer` **[string][139]**
-   `candidates` **[Array][153]&lt;[string][139]>**

## TSendTransferRequest

TSendTransferRequest is the type of the transfer request.

Type: {version: [number][140], nonce: [number][140], sender: [string][139], recipient: [string][139], amount: [number][140], senderPubKey: [string][139], signature: [string][139], payload: [string][139], isCoinbase: [boolean][141]}

### Properties

-   `version` **[number][140]**
-   `nonce` **[number][140]**
-   `sender` **[string][139]**
-   `recipient` **[string][139]**
-   `amount` **[number][140]**
-   `senderPubKey` **[string][139]**
-   `signature` **[string][139]**
-   `payload` **[string][139]**
-   `isCoinbase` **[boolean][141]**

## TSendTransferResponse

TSendTransferResponse is the type of the response of the sendTransfer.

Type: {hash: [string][139]}

### Properties

-   `hash` **[string][139]**

## TSendVoteRequest

TSendVoteRequest is the type of the request of the sendVote.

Type: {version: [number][140], nonce: [number][140], voter: [string][139], votee: [string][139], voterPubKey: [string][139], signature: [string][139]}

### Properties

-   `version` **[number][140]**
-   `nonce` **[number][140]**
-   `voter` **[string][139]**
-   `votee` **[string][139]**
-   `voterPubKey` **[string][139]**
-   `signature` **[string][139]**

## TSendVoteResponse

TSendVoteResponse is the type of the response of the sendVote.

Type: {hash: [string][139]}

### Properties

-   `hash` **[string][139]**

## TNode

TNode is the type of the node.

Type: {address: [string][139]}

### Properties

-   `address` **[string][139]**

## TGetPeersResponse

TGetPeersResponse is the type of the response of the getPeers.

Type: {Self: [TNode][159], Peers: [Array][153]&lt;[TNode][159]>}

### Properties

-   `Self` **[TNode][159]**
-   `Peers` **[Array][153]&lt;[TNode][159]>**

## TSendSmartContractResponse

TSendSmartContractResponse is the type of the response of sendSmartContract.

Type: {hash: [string][139]}

### Properties

-   `hash` **[string][139]**

## RpcMethods

RpcMethods are the API remote methods to call iotex blockchain.

### Parameters

-   `provider` **[Provider][147]**

### Examples

```javascript
import {RpcMethods, HttpProvider} from 'iotex-client-js';
const methods = new RpcMethods(new HttpProvider('http://127.0.0.1:14004'));
const height = await methods.getBlockchainHeight();
const bal = await methods.getAddressBalance('io1qyqsyqcyae8h2l4w7yr9pw9qdy26rm27jwzrzqtmqqnmt3');
```

### getBlockchainHeight

get the blockchain tip height

Returns **[Promise][143]&lt;[number][140]>**

### getAddressBalance

get the balance of an address

#### Parameters

-   `address` **[string][139]**

Returns **[Promise][143]&lt;[number][140]>**

### getAddressDetails

get the address detail of an iotex address

#### Parameters

-   `address` **[string][139]**

Returns **[Promise][143]&lt;[TAddressDetails][160]>**

### getLastTransfersByRange

get list of transfers by start block height, transfer offset and limit

#### Parameters

-   `startBlockHeight` **[number][140]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**
-   `showCoinBase` **[boolean][141]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TTransfer][152]>>**

### getTransferByID

get transfers from transaction id

#### Parameters

-   `transferID` **[string][139]**

Returns **[Promise][143]&lt;[TTransfer][152]>**

### getTransfersByAddress

get list of transfers belonging to an address

#### Parameters

-   `address` **[string][139]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TTransfer][152]>>**

### getUnconfirmedTransfersByAddress

get list of unconfirmed transfers in actpool belonging to an address

#### Parameters

-   `address` **[string][139]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TTransfer][152]>>**

### getTransfersByBlockID

get all transfers in a block

#### Parameters

-   `blkID` **[string][139]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TTransfer][152]>>**

### getLastVotesByRange

get list of votes by start block height, vote offset and limit

#### Parameters

-   `startBlockHeight` **[number][140]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TVote][161]>>**

### getVoteByID

get vote from vote id

#### Parameters

-   `voteID` **[string][139]**

Returns **[Promise][143]&lt;[TVote][161]>**

### getVotesByAddress

get list of votes belonging to an address

#### Parameters

-   `address` **[string][139]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TVote][161]>>**

### getUnconfirmedVotesByAddress

get list of unconfirmed votes in actpool belonging to an address

#### Parameters

-   `address` **[string][139]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TVote][161]>>**

### getVotesByBlockID

get all votes in a block

#### Parameters

-   `blkID` **[string][139]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TVote][161]>>**

### getLastExecutionsByRange

get list of executions by start block height, execution offset and limit

#### Parameters

-   `startBlockHeight` **[number][140]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TExecution][150]>>**

### getExecutionByID

get execution from execution id

#### Parameters

-   `executionID` **[string][139]**

Returns **[Promise][143]&lt;[TExecution][150]>**

### getExecutionsByAddress

get list of executions belonging to an address

#### Parameters

-   `address` **[string][139]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TExecution][150]>>**

### getUnconfirmedExecutionsByAddress

get list of unconfirmed executions in actpool belonging to an address

#### Parameters

-   `address` **[string][139]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TExecution][150]>>**

### getExecutionsByBlockID

get all executions in a block

#### Parameters

-   `blkID` **[string][139]**
-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TExecution][150]>>**

### getLastBlocksByRange

get list of blocks by block id offset and limit

#### Parameters

-   `offset` **[number][140]**
-   `limit` **[number][140]**

Returns **[Promise][143]&lt;[Array][153]&lt;[TBlock][162]>>**

### getBlockByID

get block by block id

#### Parameters

-   `blkID` **[string][139]**

Returns **[Promise][143]&lt;[TBlock][162]>**

### getCoinStatistic

get statistic of iotx

Returns **[Promise][143]&lt;[TCoinStatistic][163]>**

### getConsensusMetrics

get consensus metrics

Returns **[Promise][143]&lt;[TConsensusMetrics][164]>**

### getCandidateMetrics

get candidates metrics

Returns **[Promise][143]&lt;[TCandidateMetrics][165]>**

### sendTransfer

send transfer

#### Parameters

-   `request` **[TSendTransferRequest][166]**

Returns **[Promise][143]&lt;[TSendTransferResponse][167]>**

### sendVote

send vote

#### Parameters

-   `request` **[TSendVoteRequest][168]**

Returns **[Promise][143]&lt;[TSendVoteResponse][169]>**

### sendSmartContract

sendSmartContract

#### Parameters

-   `request` **[TExecution][150]**

Returns **[Promise][143]&lt;[TSendSmartContractResponse][170]>**

### getPeers

get list of peers

Returns **[Promise][143]&lt;[TGetPeersResponse][171]>**

### getReceiptByExecutionID

get receipt by execution id

#### Parameters

-   `id` **[string][139]**

Returns **[Promise][143]&lt;[TReceipt][172]>**

### readExecutionState

read execution state

#### Parameters

-   `request` **[TExecution][150]**

Returns **[Promise][143]&lt;[string][139]>**

[1]: #twallet

[2]: #properties

[3]: #tunsignedtransfer

[4]: #properties-1

[5]: #tunsignedexecution

[6]: #properties-2

[7]: #accounts

[8]: #parameters

[9]: #examples

[10]: #create

[11]: #privatekeytoaccount

[12]: #parameters-1

[13]: #add

[14]: #parameters-2

[15]: #signtransfer

[16]: #parameters-3

[17]: #signsmartcontract

[18]: #parameters-4

[19]: #tcontractopts

[20]: #properties-3

[21]: #tmethodsopts

[22]: #properties-4

[23]: #contract

[24]: #parameters-5

[25]: #methods

[26]: #deploy

[27]: #parameters-6

[28]: #preparemethods

[29]: #parameters-7

[30]: #iotx

[31]: #parameters-8

[32]: #examples-1

[33]: #sendtransfer

[34]: #parameters-9

[35]: #request

[36]: #properties-5

[37]: #response

[38]: #properties-6

[39]: #provider

[40]: #properties-7

[41]: #httpprovider

[42]: #parameters-10

[43]: #send

[44]: #parameters-11

[45]: #tcoinstatistic

[46]: #properties-8

[47]: #tblockgenerator

[48]: #properties-9

[49]: #tblock

[50]: #properties-10

[51]: #ttransfer

[52]: #properties-11

[53]: #texecution

[54]: #properties-12

[55]: #tlog

[56]: #properties-13

[57]: #treceipt

[58]: #properties-14

[59]: #tvote

[60]: #properties-15

[61]: #taddressdetails

[62]: #properties-16

[63]: #tcandidate

[64]: #properties-17

[65]: #tcandidatemetrics

[66]: #properties-18

[67]: #tconsensusmetrics

[68]: #properties-19

[69]: #tsendtransferrequest

[70]: #properties-20

[71]: #tsendtransferresponse

[72]: #properties-21

[73]: #tsendvoterequest

[74]: #properties-22

[75]: #tsendvoteresponse

[76]: #properties-23

[77]: #tnode

[78]: #properties-24

[79]: #tgetpeersresponse

[80]: #properties-25

[81]: #tsendsmartcontractresponse

[82]: #properties-26

[83]: #rpcmethods

[84]: #parameters-12

[85]: #examples-2

[86]: #getblockchainheight

[87]: #getaddressbalance

[88]: #parameters-13

[89]: #getaddressdetails

[90]: #parameters-14

[91]: #getlasttransfersbyrange

[92]: #parameters-15

[93]: #gettransferbyid

[94]: #parameters-16

[95]: #gettransfersbyaddress

[96]: #parameters-17

[97]: #getunconfirmedtransfersbyaddress

[98]: #parameters-18

[99]: #gettransfersbyblockid

[100]: #parameters-19

[101]: #getlastvotesbyrange

[102]: #parameters-20

[103]: #getvotebyid

[104]: #parameters-21

[105]: #getvotesbyaddress

[106]: #parameters-22

[107]: #getunconfirmedvotesbyaddress

[108]: #parameters-23

[109]: #getvotesbyblockid

[110]: #parameters-24

[111]: #getlastexecutionsbyrange

[112]: #parameters-25

[113]: #getexecutionbyid

[114]: #parameters-26

[115]: #getexecutionsbyaddress

[116]: #parameters-27

[117]: #getunconfirmedexecutionsbyaddress

[118]: #parameters-28

[119]: #getexecutionsbyblockid

[120]: #parameters-29

[121]: #getlastblocksbyrange

[122]: #parameters-30

[123]: #getblockbyid

[124]: #parameters-31

[125]: #getcoinstatistic

[126]: #getconsensusmetrics

[127]: #getcandidatemetrics

[128]: #sendtransfer-1

[129]: #parameters-32

[130]: #sendvote

[131]: #parameters-33

[132]: #sendsmartcontract

[133]: #parameters-34

[134]: #getpeers

[135]: #getreceiptbyexecutionid

[136]: #parameters-35

[137]: #readexecutionstate

[138]: #parameters-36

[139]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[140]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[141]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[142]: #rpcmethods

[143]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise

[144]: #twallet

[145]: #tunsignedtransfer

[146]: #tunsignedexecution

[147]: #provider

[148]: #accounts

[149]: #tcontractopts

[150]: #texecution

[151]: #tmethodsopts

[152]: #ttransfer

[153]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[154]: #request

[155]: #response

[156]: #tblockgenerator

[157]: #tlog

[158]: #tcandidate

[159]: #tnode

[160]: #taddressdetails

[161]: #tvote

[162]: #tblock

[163]: #tcoinstatistic

[164]: #tconsensusmetrics

[165]: #tcandidatemetrics

[166]: #tsendtransferrequest

[167]: #tsendtransferresponse

[168]: #tsendvoterequest

[169]: #tsendvoteresponse

[170]: #tsendsmartcontractresponse

[171]: #tgetpeersresponse

[172]: #treceipt