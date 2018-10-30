---
id: sdk-rpc-methods
title: RPC methods
---

The `rpc-methods` package allow you to make JSON RPC calls to Iotex blockchain.

Use the umbrella iotx package:

```js
import {Iotx, HttpProvider} from 'iotex-client-js';
const iotx = new Iotx(new HttpProvider('http://127.0.0.1:14004'));
const height = await iotx.rpcMethods.getBlockchainHeight();
const bal = await iotx.rpcMethods.getAddressBalance('io1qyqsqqqq26zujam2gt5cut0ggu8pa4d5q7hnrvsvace4x6');
```

Use this standalone package:

```js
import {RpcMethods, HttpProvider} from 'iotex-client-js';
const methods = new RpcMethods(new HttpProvider('http://127.0.0.1:14004'));
const height = await methods.getBlockchainHeight();
const bal = await methods.getAddressBalance('io1qyqsqqqq26zujam2gt5cut0ggu8pa4d5q7hnrvsvace4x6');
```

If you would like to make JSON RPC calls by yourself, please visit [JSON RPC](/docs/json-rpc).

Please check the following list for all the RPCs supported.

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [TCoinStatistic][1]
    -   [Properties][2]
-   [TBlockGenerator][3]
    -   [Properties][4]
-   [TBlock][5]
    -   [Properties][6]
-   [TTransfer][7]
    -   [Properties][8]
-   [TExecution][9]
    -   [Properties][10]
-   [TLog][11]
    -   [Properties][12]
-   [TReceipt][13]
    -   [Properties][14]
-   [TVote][15]
    -   [Properties][16]
-   [TAddressDetails][17]
    -   [Properties][18]
-   [TCandidate][19]
    -   [Properties][20]
-   [TCandidateMetrics][21]
    -   [Properties][22]
-   [TConsensusMetrics][23]
    -   [Properties][24]
-   [TSendTransferRequest][25]
    -   [Properties][26]
-   [TSendTransferResponse][27]
    -   [Properties][28]
-   [TSendVoteRequest][29]
    -   [Properties][30]
-   [TSendVoteResponse][31]
    -   [Properties][32]
-   [TNode][33]
    -   [Properties][34]
-   [TGetPeersResponse][35]
    -   [Properties][36]
-   [TSendSmartContractResponse][37]
    -   [Properties][38]
-   [RpcMethods][39]
    -   [Parameters][40]
    -   [Examples][41]
    -   [getBlockchainHeight][42]
    -   [getAddressBalance][43]
        -   [Parameters][44]
    -   [getAddressDetails][45]
        -   [Parameters][46]
    -   [getLastTransfersByRange][47]
        -   [Parameters][48]
    -   [getTransferByID][49]
        -   [Parameters][50]
    -   [getTransfersByAddress][51]
        -   [Parameters][52]
    -   [getUnconfirmedTransfersByAddress][53]
        -   [Parameters][54]
    -   [getTransfersByBlockID][55]
        -   [Parameters][56]
    -   [getLastVotesByRange][57]
        -   [Parameters][58]
    -   [getVoteByID][59]
        -   [Parameters][60]
    -   [getVotesByAddress][61]
        -   [Parameters][62]
    -   [getUnconfirmedVotesByAddress][63]
        -   [Parameters][64]
    -   [getVotesByBlockID][65]
        -   [Parameters][66]
    -   [getLastExecutionsByRange][67]
        -   [Parameters][68]
    -   [getExecutionByID][69]
        -   [Parameters][70]
    -   [getExecutionsByAddress][71]
        -   [Parameters][72]
    -   [getUnconfirmedExecutionsByAddress][73]
        -   [Parameters][74]
    -   [getExecutionsByBlockID][75]
        -   [Parameters][76]
    -   [getLastBlocksByRange][77]
        -   [Parameters][78]
    -   [getBlockByID][79]
        -   [Parameters][80]
    -   [getCoinStatistic][81]
    -   [getConsensusMetrics][82]
    -   [getCandidateMetrics][83]
    -   [sendTransfer][84]
        -   [Parameters][85]
    -   [sendVote][86]
        -   [Parameters][87]
    -   [sendSmartContract][88]
        -   [Parameters][89]
    -   [getPeers][90]
    -   [getReceiptByExecutionID][91]
        -   [Parameters][92]
    -   [readExecutionState][93]
        -   [Parameters][94]
-   [Request][95]
    -   [Properties][96]
-   [Response][97]
    -   [Properties][98]
-   [Provider][99]
    -   [Properties][100]
-   [HttpProvider][101]
    -   [Parameters][102]
    -   [send][103]
        -   [Parameters][104]

## TCoinStatistic

TCoinStatistic is the type of stats of the iotx coin.

Type: {height: [number][105], supply: [number][105], transfers: [number][105], votes: [number][105], executions: [number][105], aps: [number][105]}

### Properties

-   `height` **[number][105]**
-   `supply` **[number][105]**
-   `transfers` **[number][105]**
-   `votes` **[number][105]**
-   `executions` **[number][105]**
-   `aps` **[number][105]**

## TBlockGenerator

TBlockGenerator is the type that identifies the generator of the block.

Type: {name: [string][106], address: [string][106]}

### Properties

-   `name` **[string][106]**
-   `address` **[string][106]**

## TBlock

TBlock is the type of the meta data of the block.

Type: {ID: [string][106], height: [number][105], timestamp: [number][105], transfers: [number][105], votes: [number][105], executions: [number][105], generateBy: [TBlockGenerator][107], amount: [number][105], forged: [number][105], size: [number][105]}

### Properties

-   `ID` **[string][106]**
-   `height` **[number][105]**
-   `timestamp` **[number][105]**
-   `transfers` **[number][105]**
-   `votes` **[number][105]**
-   `executions` **[number][105]**
-   `generateBy` **[TBlockGenerator][107]**
-   `amount` **[number][105]**
-   `forged` **[number][105]**
-   `size` **[number][105]**

## TTransfer

TTransfer is the type of the transfer.

Type: {version: [number][105], ID: [string][106], nonce: [number][105], sender: [string][106], recipient: [string][106], amount: [number][105], senderPubKey: [string][106], payload: [string][106], isCoinbase: [boolean][108], fee: [number][105], timestamp: [number][105], blockID: [string][106], isPending: [boolean][108], signature: [string][106]?}

### Properties

-   `version` **[number][105]**
-   `ID` **[string][106]**
-   `nonce` **[number][105]**
-   `sender` **[string][106]**
-   `recipient` **[string][106]**
-   `amount` **[number][105]**
-   `senderPubKey` **[string][106]**
-   `payload` **[string][106]**
-   `isCoinbase` **[boolean][108]**
-   `fee` **[number][105]**
-   `timestamp` **[number][105]**
-   `blockID` **[string][106]**
-   `isPending` **[boolean][108]**
-   `signature` **[string][106]?**

## TExecution

TExecution is the type of the execution to be sent to the iotex blockchain.

Type: {version: [number][105], ID: [string][106], nonce: [number][105], executor: [string][106], contract: [string][106], amount: [string][106], executorPubKey: [string][106], signature: [string][106], gasLimit: [number][105], gasPrice: [string][106], timestamp: [number][105], data: [string][106], blockID: [string][106], isPending: [boolean][108]}

### Properties

-   `version` **[number][105]**
-   `ID` **[string][106]**
-   `nonce` **[number][105]**
-   `executor` **[string][106]**
-   `contract` **[string][106]**
-   `amount` **[string][106]**
-   `executorPubKey` **[string][106]**
-   `signature` **[string][106]**
-   `gasLimit` **[number][105]**
-   `gasPrice` **[string][106]**
-   `timestamp` **[number][105]**
-   `data` **[string][106]**
-   `blockID` **[string][106]**
-   `isPending` **[boolean][108]**

## TLog

TLog is the type of the log in the smart contract log.

Type: {address: [string][106], topics: [Array][109]&lt;[string][106]>, data: [string][106], blockNumber: [number][105], txnHash: [string][106], blockHash: [string][106], index: [number][105]}

### Properties

-   `address` **[string][106]**
-   `topics` **[Array][109]&lt;[string][106]>**
-   `data` **[string][106]**
-   `blockNumber` **[number][105]**
-   `txnHash` **[string][106]**
-   `blockHash` **[string][106]**
-   `index` **[number][105]**

## TReceipt

TReceipt is the type of the receipt.

Type: {returnValue: [string][106], status: [number][105], hash: [string][106], gasConsumed: [number][105], contractAddress: [string][106], logs: [Array][109]&lt;[TLog][110]>}

### Properties

-   `returnValue` **[string][106]**
-   `status` **[number][105]**
-   `hash` **[string][106]**
-   `gasConsumed` **[number][105]**
-   `contractAddress` **[string][106]**
-   `logs` **[Array][109]&lt;[TLog][110]>**

## TVote

TVote is the type of the vote.

Type: {version: [number][105], ID: [string][106], nonce: [number][105], timestamp: [number][105], voter: [string][106], votee: [string][106], voterPubKey: [string][106], signature: [string][106], blockID: [string][106], isPending: [boolean][108]}

### Properties

-   `version` **[number][105]**
-   `ID` **[string][106]**
-   `nonce` **[number][105]**
-   `timestamp` **[number][105]**
-   `voter` **[string][106]**
-   `votee` **[string][106]**
-   `voterPubKey` **[string][106]**
-   `signature` **[string][106]**
-   `blockID` **[string][106]**
-   `isPending` **[boolean][108]**

## TAddressDetails

TAddressDetails is the type of the address' account detail.

Type: {address: [string][106], totalBalance: [number][105], nonce: [number][105], pendingNonce: [number][105], isCandidate: [boolean][108]}

### Properties

-   `address` **[string][106]**
-   `totalBalance` **[number][105]**
-   `nonce` **[number][105]**
-   `pendingNonce` **[number][105]**
-   `isCandidate` **[boolean][108]**

## TCandidate

TCandidate is the type of the candidate.

Type: {address: [string][106], totalVote: [number][105], creationHeight: [number][105], lastUpdateHeight: [number][105], isDelegate: [boolean][108], isProducer: [boolean][108]}

### Properties

-   `address` **[string][106]**
-   `totalVote` **[number][105]**
-   `creationHeight` **[number][105]**
-   `lastUpdateHeight` **[number][105]**
-   `isDelegate` **[boolean][108]**
-   `isProducer` **[boolean][108]**

## TCandidateMetrics

TCandidateMetrics is the type of the candidate metrics.

Type: {candidates: [Array][109]&lt;[TCandidate][111]>, latestEpoch: [number][105], latestHeight: [number][105]}

### Properties

-   `candidates` **[Array][109]&lt;[TCandidate][111]>**
-   `latestEpoch` **[number][105]**
-   `latestHeight` **[number][105]**

## TConsensusMetrics

TConsensusMetrics is the type of the consensus metrics.

Type: {latestEpoch: [number][105], latestDelegates: [Array][109]&lt;[string][106]>, latestBlockProducer: [string][106], candidates: [Array][109]&lt;[string][106]>}

### Properties

-   `latestEpoch` **[number][105]**
-   `latestDelegates` **[Array][109]&lt;[string][106]>**
-   `latestBlockProducer` **[string][106]**
-   `candidates` **[Array][109]&lt;[string][106]>**

## TSendTransferRequest

TSendTransferRequest is the type of the transfer request.

Type: {version: [number][105], nonce: [number][105], sender: [string][106], recipient: [string][106], amount: [number][105], senderPubKey: [string][106], signature: [string][106], payload: [string][106], isCoinbase: [boolean][108]}

### Properties

-   `version` **[number][105]**
-   `nonce` **[number][105]**
-   `sender` **[string][106]**
-   `recipient` **[string][106]**
-   `amount` **[number][105]**
-   `senderPubKey` **[string][106]**
-   `signature` **[string][106]**
-   `payload` **[string][106]**
-   `isCoinbase` **[boolean][108]**

## TSendTransferResponse

TSendTransferResponse is the type of the response of the sendTransfer.

Type: {hash: [string][106]}

### Properties

-   `hash` **[string][106]**

## TSendVoteRequest

TSendVoteRequest is the type of the request of the sendVote.

Type: {version: [number][105], nonce: [number][105], voter: [string][106], votee: [string][106], voterPubKey: [string][106], signature: [string][106]}

### Properties

-   `version` **[number][105]**
-   `nonce` **[number][105]**
-   `voter` **[string][106]**
-   `votee` **[string][106]**
-   `voterPubKey` **[string][106]**
-   `signature` **[string][106]**

## TSendVoteResponse

TSendVoteResponse is the type of the response of the sendVote.

Type: {hash: [string][106]}

### Properties

-   `hash` **[string][106]**

## TNode

TNode is the type of the node.

Type: {address: [string][106]}

### Properties

-   `address` **[string][106]**

## TGetPeersResponse

TGetPeersResponse is the type of the response of the getPeers.

Type: {Self: [TNode][112], Peers: [Array][109]&lt;[TNode][112]>}

### Properties

-   `Self` **[TNode][112]**
-   `Peers` **[Array][109]&lt;[TNode][112]>**

## TSendSmartContractResponse

TSendSmartContractResponse is the type of the response of sendSmartContract.

Type: {hash: [string][106]}

### Properties

-   `hash` **[string][106]**

## RpcMethods

RpcMethods are the API remote methods to call iotex blockchain.

### Parameters

-   `provider` **[Provider][113]**

### Examples

```javascript
import {RpcMethods, HttpProvider} from 'iotex-client-js';
const methods = new RpcMethods(new HttpProvider('http://127.0.0.1:14004'));
const height = await methods.getBlockchainHeight();
const bal = await methods.getAddressBalance('io1qyqsyqcyae8h2l4w7yr9pw9qdy26rm27jwzrzqtmqqnmt3');
```

### getBlockchainHeight

get the blockchain tip height

Returns **[Promise][114]&lt;[number][105]>**

### getAddressBalance

get the balance of an address

#### Parameters

-   `address` **[string][106]**

Returns **[Promise][114]&lt;[number][105]>**

### getAddressDetails

get the address detail of an iotex address

#### Parameters

-   `address` **[string][106]**

Returns **[Promise][114]&lt;[TAddressDetails][115]>**

### getLastTransfersByRange

get list of transfers by start block height, transfer offset and limit

#### Parameters

-   `startBlockHeight` **[number][105]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**
-   `showCoinBase` **[boolean][108]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TTransfer][116]>>**

### getTransferByID

get transfers from transaction id

#### Parameters

-   `transferID` **[string][106]**

Returns **[Promise][114]&lt;[TTransfer][116]>**

### getTransfersByAddress

get list of transfers belonging to an address

#### Parameters

-   `address` **[string][106]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TTransfer][116]>>**

### getUnconfirmedTransfersByAddress

get list of unconfirmed transfers in actpool belonging to an address

#### Parameters

-   `address` **[string][106]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TTransfer][116]>>**

### getTransfersByBlockID

get all transfers in a block

#### Parameters

-   `blkID` **[string][106]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TTransfer][116]>>**

### getLastVotesByRange

get list of votes by start block height, vote offset and limit

#### Parameters

-   `startBlockHeight` **[number][105]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TVote][117]>>**

### getVoteByID

get vote from vote id

#### Parameters

-   `voteID` **[string][106]**

Returns **[Promise][114]&lt;[TVote][117]>**

### getVotesByAddress

get list of votes belonging to an address

#### Parameters

-   `address` **[string][106]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TVote][117]>>**

### getUnconfirmedVotesByAddress

get list of unconfirmed votes in actpool belonging to an address

#### Parameters

-   `address` **[string][106]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TVote][117]>>**

### getVotesByBlockID

get all votes in a block

#### Parameters

-   `blkID` **[string][106]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TVote][117]>>**

### getLastExecutionsByRange

get list of executions by start block height, execution offset and limit

#### Parameters

-   `startBlockHeight` **[number][105]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TExecution][118]>>**

### getExecutionByID

get execution from execution id

#### Parameters

-   `executionID` **[string][106]**

Returns **[Promise][114]&lt;[TExecution][118]>**

### getExecutionsByAddress

get list of executions belonging to an address

#### Parameters

-   `address` **[string][106]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TExecution][118]>>**

### getUnconfirmedExecutionsByAddress

get list of unconfirmed executions in actpool belonging to an address

#### Parameters

-   `address` **[string][106]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TExecution][118]>>**

### getExecutionsByBlockID

get all executions in a block

#### Parameters

-   `blkID` **[string][106]**
-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TExecution][118]>>**

### getLastBlocksByRange

get list of blocks by block id offset and limit

#### Parameters

-   `offset` **[number][105]**
-   `limit` **[number][105]**

Returns **[Promise][114]&lt;[Array][109]&lt;[TBlock][119]>>**

### getBlockByID

get block by block id

#### Parameters

-   `blkID` **[string][106]**

Returns **[Promise][114]&lt;[TBlock][119]>**

### getCoinStatistic

get statistic of iotx

Returns **[Promise][114]&lt;[TCoinStatistic][120]>**

### getConsensusMetrics

get consensus metrics

Returns **[Promise][114]&lt;[TConsensusMetrics][121]>**

### getCandidateMetrics

get candidates metrics

Returns **[Promise][114]&lt;[TCandidateMetrics][122]>**

### sendTransfer

send transfer

#### Parameters

-   `request` **[TSendTransferRequest][123]**

Returns **[Promise][114]&lt;[TSendTransferResponse][124]>**

### sendVote

send vote

#### Parameters

-   `request` **[TSendVoteRequest][125]**

Returns **[Promise][114]&lt;[TSendVoteResponse][126]>**

### sendSmartContract

sendSmartContract

#### Parameters

-   `request` **[TExecution][118]**

Returns **[Promise][114]&lt;[TSendSmartContractResponse][127]>**

### getPeers

get list of peers

Returns **[Promise][114]&lt;[TGetPeersResponse][128]>**

### getReceiptByExecutionID

get receipt by execution id

#### Parameters

-   `id` **[string][106]**

Returns **[Promise][114]&lt;[TReceipt][129]>**

### readExecutionState

read execution state

#### Parameters

-   `request` **[TExecution][118]**

Returns **[Promise][114]&lt;[string][106]>**

## Request

Request is the type of the request sent from the Provider.

Type: {method: [string][106], params: [Array][109]&lt;any>}

### Properties

-   `method` **[string][106]**
-   `params` **[Array][109]&lt;any>**

## Response

Response is the response type received by the Provider.

Type: {result: any, error: {code: [number][105], message: [string][106]}}

### Properties

-   `result` **any**
-   `error` **{code: [number][105], message: [string][106]}**
-   `error.code` **[number][105]**
-   `error.message` **[string][106]**

## Provider

Provider is the network provider interface of iotex backend.

### Properties

-   `send` **function (request: [Request][130]): [Promise][114]&lt;[Response][131]>**

## HttpProvider

Provider is the network provider of iotex backend that is implemented in HTTP.

### Parameters

-   `url` **[string][106]**
-   `timeout` **[number][105]?**

### send

send makes an xhr call to the url.

#### Parameters

-   `request` **[Request][130]**

Returns **[Promise][114]&lt;[Response][131]>**

[1]: #tcoinstatistic

[2]: #properties

[3]: #tblockgenerator

[4]: #properties-1

[5]: #tblock

[6]: #properties-2

[7]: #ttransfer

[8]: #properties-3

[9]: #texecution

[10]: #properties-4

[11]: #tlog

[12]: #properties-5

[13]: #treceipt

[14]: #properties-6

[15]: #tvote

[16]: #properties-7

[17]: #taddressdetails

[18]: #properties-8

[19]: #tcandidate

[20]: #properties-9

[21]: #tcandidatemetrics

[22]: #properties-10

[23]: #tconsensusmetrics

[24]: #properties-11

[25]: #tsendtransferrequest

[26]: #properties-12

[27]: #tsendtransferresponse

[28]: #properties-13

[29]: #tsendvoterequest

[30]: #properties-14

[31]: #tsendvoteresponse

[32]: #properties-15

[33]: #tnode

[34]: #properties-16

[35]: #tgetpeersresponse

[36]: #properties-17

[37]: #tsendsmartcontractresponse

[38]: #properties-18

[39]: #rpcmethods

[40]: #parameters

[41]: #examples

[42]: #getblockchainheight

[43]: #getaddressbalance

[44]: #parameters-1

[45]: #getaddressdetails

[46]: #parameters-2

[47]: #getlasttransfersbyrange

[48]: #parameters-3

[49]: #gettransferbyid

[50]: #parameters-4

[51]: #gettransfersbyaddress

[52]: #parameters-5

[53]: #getunconfirmedtransfersbyaddress

[54]: #parameters-6

[55]: #gettransfersbyblockid

[56]: #parameters-7

[57]: #getlastvotesbyrange

[58]: #parameters-8

[59]: #getvotebyid

[60]: #parameters-9

[61]: #getvotesbyaddress

[62]: #parameters-10

[63]: #getunconfirmedvotesbyaddress

[64]: #parameters-11

[65]: #getvotesbyblockid

[66]: #parameters-12

[67]: #getlastexecutionsbyrange

[68]: #parameters-13

[69]: #getexecutionbyid

[70]: #parameters-14

[71]: #getexecutionsbyaddress

[72]: #parameters-15

[73]: #getunconfirmedexecutionsbyaddress

[74]: #parameters-16

[75]: #getexecutionsbyblockid

[76]: #parameters-17

[77]: #getlastblocksbyrange

[78]: #parameters-18

[79]: #getblockbyid

[80]: #parameters-19

[81]: #getcoinstatistic

[82]: #getconsensusmetrics

[83]: #getcandidatemetrics

[84]: #sendtransfer

[85]: #parameters-20

[86]: #sendvote

[87]: #parameters-21

[88]: #sendsmartcontract

[89]: #parameters-22

[90]: #getpeers

[91]: #getreceiptbyexecutionid

[92]: #parameters-23

[93]: #readexecutionstate

[94]: #parameters-24

[95]: #request

[96]: #properties-19

[97]: #response

[98]: #properties-20

[99]: #provider

[100]: #properties-21

[101]: #httpprovider

[102]: #parameters-25

[103]: #send

[104]: #parameters-26

[105]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[106]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[107]: #tblockgenerator

[108]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[109]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[110]: #tlog

[111]: #tcandidate

[112]: #tnode

[113]: #provider

[114]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise

[115]: #taddressdetails

[116]: #ttransfer

[117]: #tvote

[118]: #texecution

[119]: #tblock

[120]: #tcoinstatistic

[121]: #tconsensusmetrics

[122]: #tcandidatemetrics

[123]: #tsendtransferrequest

[124]: #tsendtransferresponse

[125]: #tsendvoterequest

[126]: #tsendvoteresponse

[127]: #tsendsmartcontractresponse

[128]: #tgetpeersresponse

[129]: #treceipt

[130]: #request

[131]: #response