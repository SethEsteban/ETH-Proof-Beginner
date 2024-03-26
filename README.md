# ETH-Proof-Beginner
 This Solidity program is a simple program that creates and burns tokens. It shows the simple functions of creating one and burning one, for those who are new can grasp the idea behind it.

 ## Description
 This program is created using Solidity, used in developing smart contracts in Ethereum. This program has two functions, one to mint and the other to burn. The purpose of this program is to show to those who are still new how minting and burning tokens work, to have a grasp on the whole idea by having this simple program.

 ## Getting Started
 ### Executing Program
 To start this program, you can use Remix, an online IDE (remix.ethereum.org)
 From there click the "Start Coding Button". Name and save your file name with .sol as your extension, then copy and paste the code below:

```solidity
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public tokenName = "META";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;
    
    // mint function
    function mint(address _address, uint _value)public{
      totalSupply += _value;
      balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value)public{
      if (balances[_address] >= _value){
      totalSupply -= _value;
      balances[_address] -= _value;
      }
    
    }
}

```
Once done, click the Solidity Compiler on the left side, and click Compile (Your FileName) .sol. Next, just below that, click Deploy & run transactions button, click deploy, then just below, click the arrow with the name of your contract and address in it. To mint tokens, copy the given address and paste it on mint, add desired value and click transact. The same procedure is done for burning tokens but this time it subtracts. To see the number of tokens, click totalSupply. For balances, paste the given address and click call.

## Authors
Seth Esteban
@SethEsteban

## License
This project is licensed under the MIT License 
