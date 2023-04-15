# Accio.nft

Cross Chain Liquidity for L2-based NFTs

## Project Description

- TODO

## Demo

- TODO: add link to the demo video
- TODO: add link to the slide deck


## Development

### Hyperlane

- TODO

### Smart contracts
https://github.com/2023ethtokyoteam1/accio-nft-contracts

The `buy` function on the `LiquidityAggregator` contract is the initial entrypoint that triggers the cross-chain liquidity aggregation and NFT purchase flow. It stores the user's request within the contract storage, fetches user funds on the local chain if needed, and sends interchain messages to the `LiquidityAggregator`s on the remote chains. Once the remote `LiquidityAggregator` receives the message, it gets the user's funds on the remote chain and calls `transferRemote` on the [`HypERC20`](https://docs.hyperlane.xyz/docs/apis-and-sdks/warp-api#interface) token to send them over to the origin chain. Upon a successful interchain transfer, the `handleWithToken` function on the origin chain's `LiquidityAggregator` is called and if the funds are all aggregated, an NFT purchase is executed.

#### Steps
1. Clone the [contract repo](https://github.com/2023ethtokyoteam1/accio-nft-contracts).
2. `yarn init`
3. `hardhat compile`
4. TODO: deploy steps


### Frontend

- TODO


