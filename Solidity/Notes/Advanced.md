# [Yt Video](https://www.youtube.com/watch?v=EhPeHeoKF88)
# Modifier:
- Function Modifiers are used to modify the behaviour of a function. For example to add a prerequisite to a function.
  - Payable: Payable function modifiers provide a mechanism to receive funds in your smart contract. These functions are annotated with the payable keyword.

# Enum:
- Enums restrict a variable to have one of only a few predefined values.
- Used to keep track of statuses or states (vacant and occuped)
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

// Showcase Ether Payment transfers, Enums, Modifiers , Events & Visibility

contract HotelRoom {
    enum Statuses {                                                                       // Declared enum (Status of the Room)
        Vacant,
        Occupied
    }
    Statuses public currentStatus;                                                        // Variable which checks the current Status

    event Occupy(address _occupant, uint256 _value);                                      

    address payable public owner;                                                         // State variable which specifies the Ethereum address of the person who created this samrt contract

    constructor() {
        owner = payable(msg.sender);
        currentStatus = Statuses.Vacant;
    }

    modifier onlyWhileVacant() {                                                          // *Used to make fucntion code cleaner (just mention the modifier)
        require(currentStatus == Statuses.Vacant, "Currently occupied.");                 // Checks if satement is true then only executes the function
        _;
    }

    modifier costs(uint256 _amount) {
        require(msg.value >= _amount, "Not enough Ether provided.");
        _;
    }

    function book() public payable *onlyWhileVacant costs(2 ether) {                           // Books the hotel room
        currentStatus = Statuses.Occupied;
        
        // Check Status
        (bool sent, bytes memory data) = owner.call{value: msg.value}("");
        require(sent);                                                                        
        
        // alert issues (history of bookings)
        emit Occupy(msg.sender, msg.value);
    }
}
```
