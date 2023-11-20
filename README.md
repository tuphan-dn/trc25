# VRC25 Specifications

## Installation

```bash
npm install vrc25
```

## Usage

```ts
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

import "vrc25/contracts/VRC25.sol";

contract MyToken is VRC25 {
  constructor() VRC25("MyToken", "TKN", 9) {
    _mint(msg.sender, 1000000 * 10 ** 9); // You can remove this line if doesn't want to initial mint
  }

  function _estimateFee(
    uint256 value
  ) internal view virtual override returns (uint256) {
    // We will require the sender pay nothing in this example.
    // In case of avoiding spams, you can charge a small number of tokens.
    return value * 0;
  }
}
```

## How to call `apply`/`charge` to the VRC25 Issuer?

You can use the GUI here [https://viction.tuphan.dev](https://viction.tuphan.dev) which supports both testnet and mainnet.

## LICENSE

Apache-2.0
