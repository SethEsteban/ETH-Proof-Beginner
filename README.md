# ETH-Proof-Beginner
 This Solidity program is a simple program that creates tokens. It shows the simple functions of creating one where those who are new can grasp the idea behind it.

 ## Description
 This program is created using Solidity, used in developing smart contracts in Ethereum. This program has two functions, one to mint and the other to burn. The purpose of this program is to show to those who area still new how minting and burning tokens work, to have a grasp on the whole idea by having this simple program.

 ## Getting Started
 ### Executing Program
 To start this program, you can use Remix, an online IDE (remix.ethereum.org)
 From there click the "Start COding Button". Name and save your file name with .sol as your extensions, then copy and paste the code below:

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
 

## Authors
Seth Esteban
@SethEsteban

## License
This project is licensed under the MIT License 
