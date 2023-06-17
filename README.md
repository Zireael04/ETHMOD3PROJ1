# ETHMOD3PROJ1
# Creating a Token
This Solidity application is a straightforward token generator that makes use of the fundamental capabilities of Solidity by generating and managing token transactions in Ethereum. This project's goal is to make it easier for new users to comprehend how to run a program in Solidity and how it functions.

## Description

In order to demonstrate how Solidity works, this software creates or distributes tokens to accounts using the fundamental Solidity features. Solidity is essentially a programming language used to create smart contracts—programs that are stored on a blockchain—within the Ethereum blockchain. This application has features that may be used at the user's expense and allow them to produce token values and restore their balances to the user's account's starting balance. Through the addition and subtraction of their sums, they will be able to change the values of a number of addresses or tokens. This application will give a general understanding of how the Solidity programming language interacts with the Ethereum blockchain.

## Getting Started with ETH

### IDE

To run this program, you should use Remix, which is an online Solidity IDE. https://remix.ethereum.org/.

### Executing program

Depending on how you want to use the IDE, click the "+" button in the sidebar on the left to either create a new workspace for yourself or a fresh workspace within the currently selected workspace. Save the document afterwards with a.sol extension (for example, HotDogger.sol). The code below should be copied and pasted into the file:
```
contract MyToken {

    // public variables here
    string public tokenName = "GoX";
    string public tokenAbbrv = "G10";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public wallet;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        wallet[_address] += _value;
    }

    // burn function
    function burn (address _address ,uint _value) public {
        if (wallet[_address] >= _value) {
        totalSupply -= _value;
        wallet[_address] -= _value;
    }
  }
}
```
* Select the "Solidity Compiler" tab in the left-hand sidebar to compile the code. Click the "Compile myToken.sol" button after ensuring that the "Compiler" option is set to "0.8.18" (or another suitable version).
* After the contract has been successfully compiled, you may deploy it by selecting the "Deploy & Run Transactions" tab from the left-hand sidebar, which is located right below the Solidity Compiler tab. Click the "Deploy" button after selecting the "myToken" contract from the drop-down menu.
* From there, you may view the contract that has been deployed and perform transactions using the Mint function, which works to add tokens, the Burn function, which subtracts tokens from addresses, and the Balance function, which shows the tokens' current balance.
* 
## Author

Keith Goten Bon Supan
supangoten4@gmail.com


