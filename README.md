# Token Implementation & Creation

this is a Solidity Project "Token Implementation & Creation"
program.





## Description

With the sign MTK, this smart contract introduces MyToken, a unique ERC20 token. The contract has features for keeping a balance ledger current in addition to minting and burning tokens.
## Getting Started
## Executing Program

First to open any Browser and to open Remix IDE, it's an online Solidity Platform.
link - https://remix.ethereum.org/.

then create a new file and file extension is .sol and save it. then copy and paste the code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {

    // Public variables
    string public name = "MyCustomToken";
    string public symbol = "MCT";
    uint public totalSupply = 0;

    // Mapping to track balances
    mapping (address => uint) public balances;

    // Function to mint new tokens
    function mintTokens(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // Function to burn tokens
    function burnTokens(address _address, uint _value) public {
        require(balances[_address] >= _value, "Insufficient balance");
        
        totalSupply -= _value;
        balances[_address] -= _value;
    }

}


## Authors

Swati Joshi


## License

This project is licensed under the MIT License- see the LICENSE.md file for details.
