# My Token

This Solidity contract, named MyToken, is designed to implement a basic token functionality with minting and burning capabilities.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a single function that returns the string "Hello World!". This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT

pragma solidity 0.8.18;

contract MyToken 
{


//1.public variables that store the details about your coin

    string public tokenName = "My New Token";
    
    string public tokenAbbrv = "MNT";
    
    uint public totalSupply = 0;

//2.mapping of addresses to balances 

    mapping(address => uint) public balances;

//3.mint function
//increases the total supply by that number and increases the balance 
//of the “sender” address by that amount

    function mint(address _address,uint _value) public
    {
        totalSupply += _value;
        balances[_address] += _value;
    }

//4.burn function

    function burn(address _address,uint _value) public{

//  conditionals to make sure the balance of "sender" is greater than or equal 
// to the amount that is supposed to be burned.

        if(balances[_address] >= _value)
        {
        totalSupply -= _value;
        balances[_address] -= _value;
        }
    }

}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the  function.Finally, click on the "transact" button to execute the function and retrieve the "My New Token" message.

## Authors

Vivek Kumar
