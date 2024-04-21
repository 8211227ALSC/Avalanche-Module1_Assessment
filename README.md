# ErrorHandling
Error handling mechanisms are techniques used in programming to manage and respond to errors, exceptions, or unexpected situations that may arise during the execution of code. In the context of Solidity smart contracts, error handling mechanisms are crucial for ensuring the robustness and reliability of the contracts. By using error handling mechanisms effectively, Solidity developers can ensure that their smart contracts behave as intended, handle unexpected situations gracefully, and maintain the integrity of the blockchain network.

## Description
Sure! This Solidity smart contract, named ErrorHandling, demonstrates various methods of error handling within Ethereum smart contracts. This contract demonstrates the use of require, assert, and revert statements for different types of error handling in Solidity smart contracts.

### Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:


```// SPDX-License-Identifier: MIT

pragma solidity ^0.8.0;

contract ErrorHandling {
    uint256 public value;

    function setValue(uint256 _value) public {
        // Require statement - checks conditions and throws an error if not met
        require(_value > 10, "Number must be greater than 10");
        
        // Assert statement - used to ensure internal state is as expected, otherwise throws an error
        assert(_value != 200);
        
        // Revert statement - aborts execution and reverts state changes if condition is not met
        if (_value == 100) {
            revert("Number cannot be 100");
        }

        value = _value;
    }
}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile myToken.sol" button.

To deploy the contract, click on the "Deploy and Run Transactions" button. This will open a new window that allows you to deploy the contract. Do not forget to select the “MyToken” contract before deploying.

In the deployment window “Deployed Contracts”, set the parameters for the balance, mint, and burn functions.

To mint new tokens, input the address of the recipient and the number of tokens you want to mint and click transact.

To burn tokens, input the address of the recipient and the number of tokens you want to burn and click transact.

To see current balances of the address, input the address of the recipient and the number of tokens you want to mint and click call. You can also see the total supply by clicking the “totalSupply” button.

#### Authors
NTCIAN Ann Loraine S. Ching | Discord @annching

##### License
This project is licensed under the MIT License - see the LICENSE.md file for details.
