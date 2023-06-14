# Variables and Data-types:
## Types of variables:
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

## String:
- Store Chaarcters and an array of words
```solidity
pragma solidity ^0.8.0;

contract Variables {
      string public myString = "Hello, World!";
      bytes32 public myBytes32 = "Hello, World!";       //Treats string like an array
    }
```

## Addresses:
- Acts as a Username on the BlockChain
```solidity
pragma solidity ^0.8.0;

contract Variables {
      address public myAddress = 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2;
    }
```

## Struct (Structures):
- Complex Object with mutiple values inside of it
```solidity
pragma solidity ^0.8.0;

contract Variables {
      struct MyStruct {
        uint256 myUint256;
        string myString;
    }

    MyStruct public myStruct = MyStruct(1, "Hello, World!");
    }
```
