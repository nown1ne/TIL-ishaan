# Array:
- Array is a data structure, which stores a fixed-size sequential collection of elements of the same type.

```solidity
pragma solidity ^0.8.0;

contract Arrays {
    uint256[] public uint256Array = [1, 2, 3];                            // 1-D Integer array
    string[] public stringArray = ["apple", "banana", "carrot"];          // 1-D String array
    string[] public values;
    uint256[][] public array2D = [[1, 2, 3], [4, 5, 6]];                  // 2-D Integer array

    function addValue(string memory _value) public {
        values.push(_value);                                              //adds _value at the back of the string
    }

    function valueCount() public view returns (uint256) {                 // returns number of elements in the values array
        return values.length;
    }
}
```
