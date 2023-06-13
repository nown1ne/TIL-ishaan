# Solidity:
- Solidity is an object-oriented programming language for implementing smart contracts on various blockchain platforms, most notably, Ethereum. 

## IDE:
- [remix IDE](remix.ethereum.org)

## Syntax:
- Use Captial Letter for Samrt Contract File name: `Counter.sol`
- .sol is the extension used in solidity langauge:

### Pragma:
- pragma helps you tell the computer which version of Solidity you want to use for your smart contract.
```solidity
pragma solidity ^0.8.0;  // Declare the solidity programming language verison we are using (version 0.8.0) to run this file

contract Counter{
    // code goes here..
    
}
```
- Contracts are like objects in Solidity, they can be called and are the basic units which can be reused.

### Declaring State Variables:
- They are delared in smart contracts, not in functions.
  - As solidity is staticly typed we need to specify a data type
- Like uint (positive integers) / int (neg+pos intergers)
```solidity
pragma solidity ^0.8.0;

contract Counter{
    uint count;     //1,2,3....
                    // cannot be -1, -2....
}
```

### Declaring Functions:
- Piece of code which can be reused and called over and over again
```solidity
pragma solidity ^0.8.0;

contract Counter{
    uint count;
    
    function getCount() public {      // Public specifies that we can call this function outside the smart contract
        return count;
    }

}
```
