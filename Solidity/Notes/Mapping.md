# Mapping:
- Mapping in Solidity acts like a hash table or dictionary in any other language. 
- These are used to store the data in the form of key-value pairs, a key can be any of the built-in data types but reference types are not allowed while the value can be of any type. 
- Mappings are mostly used to associate the unique Ethereum address with the associated value type.

-- Protip0> TO differentiate local and State Variables:
  - Write local varibales like this -> _local
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Mappings {
    //mappind(key => value) myMapping;
    mapping(uint256 => string) public names;
    mapping(uint256 => Book) public books;
    mapping(address => mapping(uint256 => Book)) public myBooks;          // 2-D Mapping (Nested Mapping used for Tokens and NFT's)

    struct Book {
        string title;
        string author;
    }

    constructor() {                                                       //Assign Values to the mapping (add values to mapping)
        names[1] = "Adam";
        names[2] = "Bruce";
        names[3] = "Carl";
    }

    function addBook(                                                     // Add books to the Structure
        uint256 _id,
        string memory _title,
        string memory _author
    ) public {
        books[_id] = Book(_title, _author);
    }

    function addMyBook(
        uint256 _id,
        string memory _title,
        string memory _author
    ) public {
        myBooks[msg.sender][_id] = Book(_title, _author);
    }
}
```
