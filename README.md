
## MyToken

This Solidity contract defines a custom token named "ASHWIN" with the abbreviation "ASH". It allows for minting and burning of tokens while keeping track of balances associated with different addresses.

## Description

The MyToken contract is a simple implementation of a custom token on the Ethereum blockchain. It includes functionalities for minting and burning tokens, as well as tracking the total supply and individual balances. This contract can serve as a basic template for more advanced token contracts.

## Requirements

1.Public Variables: The contract includes public variables to store details about the token (Token Name, Token Abbrv., Total Supply).

2.Mapping of Addresses to Balances: A mapping is used to associate addresses with their respective token balances.

3.Mint Function: Increases the total supply and the balance of the specified address.

4.Burn Function: Decreases the total supply and the balance of the specified address, with conditions to ensure sufficient balance.

## Getting Started

Executing the Program

To run this program, you can use Remix, an online Solidity IDE. Follow these steps to get started:

1.Open Remix: Visit the Remix website at Remix.

2.Create a New File: Click on the "+" icon in the left-hand sidebar to create a new file. Save the file with a .sol extension (e.g., MyToken.sol).

3.Copy and Paste Code: Copy and paste the following code into the file:

```

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

  // public variables here
  string public tokenName = "ASHWIN";
  string public tokenAbbrv = "ASH";
  uint totalSupply = 0;
    
 // mapping variable here
   mapping(address => uint) public balances;
    
 // mint function
   function mint(address _address, uint _value) public {
  totalSupply += _value;
 balances[_address] += _value;
 } 

  // burn function
  function burn(address _address, uint _value) public {
  if (balances[_address] >= _value) {
  totalSupply -= _value;
  balances[_address] -= _value;
  }
  }
  }
```

## Compile the Code:

1.Click on the "Solidity Compiler" tab in the left-hand sidebar.

2.Ensure the "Compiler" option is set to "0.8.18" (or another compatible version).

3.Click on the "Compile MyToken.sol" button.

## Deploy the Contract:

1.Click on the "Deploy & Run Transactions" tab in the left-hand sidebar.

2.Select the "MyToken" contract from the dropdown menu.

3.Click on the "Deploy" button.

## Interact with the Contract:

1.Use the "mint" function to add tokens to an address.

2.Use the "burn" function to remove tokens from an address, ensuring the address has a sufficient balance.

## Authors

- Dev Sagar - [@DevSGithub2](https://github.com/DevSGitub2)



## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
                                                                                                                                                                    
