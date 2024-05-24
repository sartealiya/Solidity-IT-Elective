# Solidity-IT-Elective

This project was made as a token for our IT Elective course.

## Description
This application is a smart contract built with Solidity. One of the functions of the contract is to add a certain amount of value to the address's balance and total supply. The value is subtracted from the address's balance and the total supply as the other function. 

## Getting Started

You can use the online Solidity IDE remix to execute this application. To Get started, go to https://remix.ethereum.org/.

To create a new file, navigate to the Remix website and click the "file" button located in the left-hand sidebar. Save the file with a.sol extension (solidToken.sol, for example). The code below can be copied and pasted into the document.

pragma solidity 0.8.6;

contract MyToken {
    string public tokenName = "SOLID";
    string public tokenAbbrv = "SLD";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint (address _address, uint _value) public {
      totalSupply +=_value;
      balances[_address] +=_value;
  }

    function burn (address _address, uint _value) public {
      if (balances[_address] >=_value){
        totalSupply -=_value;
        balances[_address] -=_value;
      }
    }
  }

Select the "Solidity Compiler" tab from the sidebar on the left to begin compiling the code. Click "Compile solidToken.sol" after ensuring that the "Compiler" option is selected to "0.8.6" (or another compatible version).

Selecting the "Deploy & Run Transactions" tab from the left-hand sidebar will allow you to deploy the contract after the code has been compiled. Click the "Deploy" button after choosing the "MyToken" contract from the dropdown menu.

Click the arrow down button to the right of the mint button to input the value you want to mint before using the mint function. Once the value has been inserted, copy the address and paste it into the "_address" field from the "Account" right-hand sidebar at the top. At this point, you can call the balance and obtain the whole supply by clicking the "Transact" button. The burn function is executed in the same way as the mint function, but the outcomes are different.


Author
NTC Izzy

@izzysarte23
