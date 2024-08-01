# Raindex Adapter for DefiLlama

This repository contains an adapter that enables DefiLlama to fetch and display data from Raindex. The adapter supports multiple chains and fetches Total Value Locked (TVL) and volume data for specified contracts.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Supported Chains](#supported-chains)
- [Methodology](#methodology)
- [Contributing](#contributing)
- [License](#license)

## Installation

To install the necessary dependencies, run:

```bash
npm install
```

## Usage

The adapter fetches TVL and volume data for Raindex. The data is fetched from the specified contracts on different chains and can be used to integrate with DefiLlama.

## Example

To use the adapter, you can import it and call the fetch method with the appropriate options.

```
import adapter from './path_to_adapter';

// Example usage
const options = {
  endTimestamp: Date.now() / 1000,
  getEndBlock: async (chain) => {/* implementation to get block number */}
};

const result = await adapter.breakdown.v1[CHAIN.ETHEREUM].fetch(options);
console.log(result);
```

## Supported Chain

The adapter currently supports the following chains:

- Ethereum
- Polygon
- Arbitrum
- Binance Smart Chain (BSC)
- Flare
- Base

## Methodology

The adapter counts the number of tokens in specified contracts and calculates their volume. It uses the following methods:

- fetchTVL: Fetches the Total Value Locked (TVL) by counting the balance of tokens in the specified contracts.
- fetchVolume: Fetches the volume of tokens by counting the total supply in the specified contracts (using a placeholder ABI for volume fetching).

  



