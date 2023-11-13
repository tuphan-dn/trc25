# VRC25 Specifications

## Installation

```bash
npm install vrc25
```

## Usage

```js
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

import "vrc25/contracts/VRC25.sol";

contract MyToken is VRC25 {
  constructor() VRC25("MyToken", "TKN", 9) {}

  function _estimateFee(
    uint256 value
  ) internal view virtual override returns (uint256) {
    // We will require the sender pay nothing in this example.
    // In case of avoiding spams, you can charge a small number of tokens.
    return value * 0;
  }
}
```
