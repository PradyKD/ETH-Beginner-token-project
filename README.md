# Tokens in Solidity Smart Contract 

The purpose of this solidity smart contract code is to mint tokens in a contract, with the additional functionality of burning those coins as well.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract creates a digital token with its metadata as name, abbreviation, and total supply. This contract gives the functionality to mint coins as well as burn it with respect to the available supply of tokens at a specified address. 

## Getting Started

The code starts with defining the metadata for the digital token, which includes its name, abbreviation, and its total supply. The next attribute is 'balances', which is mapping that maps the address with the available tokens at that location. 
To mint the tokens, this code has the mint-function which takes parameters as address(where the tokens are to be stored) and value(the no. of tokens to be minted). 
Similar to mint-function, we have the burn-function which deducts the specified no. of tokens from the specified address. This function deducts coin with a condition that the value to be deducted must be less than or equal to the amount held at the address. 


### Executing program

* Compile the contract.
* Deploy the contract
* Access the fucntionalities at the "Deployed/Unpinned Contracts" section
```
    // mapping variable here
    mapping (address => uint) public balance;

    // mint function
    function mint(address _address, uint _value) public  {
        totalSupply += _value;
        balance[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public  {
        if (balance[_address] >= _value) {
        totalSupply -= _value;
        balance[_address] -= _value;
        }
    }
```

## Authors

Contributors names and contact info

Pradyumna 
https://github.com/PradyKD

