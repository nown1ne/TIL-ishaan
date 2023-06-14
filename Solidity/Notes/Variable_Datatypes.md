# Variables:
- **State Variables:**
  - This variables value is stored on a blockchain, and can be called insdie the entire smart contract.
- **Local Variables:**
  - They exit inside Solidity Fucntions

```solidity
pragma solidity ^0.8.0;

contract Variables {
    // State Variables
    int256 public myInt = 1;          // 256 bytes (uint == uint256)
    uint256 public myUint256 = 1;
    uint8 public myUint8 = 1;         // 8 bytes 
    
    
    // Local Variables
    function getValue() public pure returns (uint256) {       //pure-> Doesn't Modify the blockchain in any way
        uint256 value = 1;
        return value;
    }
}
```
