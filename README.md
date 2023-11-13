# VRC25 Specifications

## Installation

```bash
npm install vrc25
```

## Usage

```js
pragma solidity ^0.8.9;

import {VRC25} from "vrc25/contracts/VRC25.sol";

contract MyToken is VRC25 {
  constructor() VRC25("MyToken", "TKN", 9) {}
}
```
