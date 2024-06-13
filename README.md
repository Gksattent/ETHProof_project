# Project Title

Create a Token.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a single function that returns the string "MyToken". This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Installing

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

### Executing program

  To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the MyToken function. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "MyToken" function. Finally, click on the "transact" button to execute the function and retrieve the "totalvalue" message.
````




// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
   
    string public tokenName = "META";
    string public tokenAbbrev = "MTA";
    uint public totalSupply = 0;


    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
function burn (address _address, uint _value) public {
       if (balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}
}
``````
## Author
Gaurav Kumar Singh
gauravattent@gmail.com

## license
This project is licensed under the MIT License - see the LICENSE.md file for details
