# Solidity:
- Solidity is an object-oriented programming language for implementing smart contracts on various blockchain platforms, most notably, Ethereum. 

## IDE:
- [remix IDE](remix.ethereum.org)

## Syntax:
- Use Captial Letter for Samrt Contract File name: `Counter.sol`
- `.sol` is the extension used in solidity langauge:

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
- Here:
    - getcount() return the count value
        - Reads are free on Blockchain
    - incrementCount() increments the count by one
        - Whenever we change values in blockchain we have to pay Gas (Writes cost Gas)
```solidity
pragma solidity ^0.8.0;

contract Counter{
    uint count;
    
    // function getCount() public {      // Public specifies that we can call this function outside the smart contract
    //     return count;
    // }
    
    // function getCount() internal {      // Internal specifies that we can call this function only inside the smart contract
    //     return count;
    // }
    
    function getCount() public view returns(uint) {      // Specifies the return type of the function
        return count;
    }
    
    function incrementCount() public {
        count++;
    }          
}
```

### Declaring Constructors:
- Special functions for each smart contract that gets run only once whenever the contract is deployed to the blockchain
```solidity
pragma solidity ^0.8.0;

contract Counter {
    uint256 public count ;      //makes getcount redundant, as this displays count 

    constructor() public {      // No arguments, public so we can call the contructor when contract is initialised 
        count = 0;              // Set count to default value
    }
    
    // function getCount() public view returns (uint256) {
    //     return count;
    // }

    function incrementCount() public {
        count++;
    }
}
```

### Initialization of Variables:
```solidity
pragma solidity ^0.8.0;

contract Counter {
    uint256 public count = 0;      // Sets count to 0 and makes constructor redundant

    function incrementCount() public {
        count++;
    }
}
```

## Transaction for above funtion
```
Address             0xa131AD247055FD2e2aA8b156A11bdEc81b9eAD95
status	            true Transaction mined and execution succeed
transaction hash	0xea13a25019fc29ae76ba4a4d5b2be1a7f1686aaf59688e26e1c7af8e375d0550
from	            0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2
to	                Counter.(constructor)
gas	                152358 gas
transaction cost	132511 gas 
execution cost	    73937 gas 
input	            0x608...20033
decoded input	    {}
decoded output	    - 
logs	            []
val	                0 wei
```
