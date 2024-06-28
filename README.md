# PROJECT-CREATE-A-TOKEN
This Solidity program showcases key programming concepts such as variable declaration, mappings, functions, and conditional expressions. It demonstrates my foundational skills in blockchain development, acquired from Metacrafters' fundamental Ethereum course, by implementing a simple Token system.

# DESCRIPTION
This program creates MyToken, a simple smart contract for a digital currency on the Ethereum network. It defines the token's name, abbreviation, and total supply, all of which are public. It uses a mapping to track balances for each address, ensuring accurate transactions. The contract includes two main functions: mint and burn. The mint function adds tokens to a given address, increasing both the total supply and the address's balance. The burn function removes tokens from an address, decreasing both the total supply and the address's balance, with safeguards to prevent burning more tokens than are available.

# GETING STARTED
EXECUTING THE PROGRAM

To execute this program, use Remix, an online Solidity IDE. Visit [Remix](https://remix.ethereum.org/). Once there, click the "+" symbol in the left-hand sidebar to create a new file. Save the file as HelloWorld.sol. Copy and paste the code below into the file.

    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;
    
    contract MyToken {

    // public variables here
    string public tokenName = "META";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address addr, uint value) public{
        totalSupply += value;
        balances[addr] += value;
    }

    // burn function
    function burn(address addr, uint value) public{
        if(balances[addr] >= value){
            totalSupply -= value;
        balances[addr] -= value;
        }
        
    }

To compile the code, select the "Solidity Compiler" tab from the left sidebar. Set the "Compiler" option to "0.8.18" (or a suitable version). To deploy the contract, go to the "Deploy & Run Transactions" tab. Choose the name of contract from the dropdown menu and click "Deploy". To interact with the contract, click the name of the contract in the left-hand sidebar, then click the name of the function. Finally, click "transact" to get the message.

# AUTHORS
Metacrafter Student Ivanne Cres Yabut https://x.com/ivanne_cres
# LICENSE 
This project is licensed under the Ivanne Cres Yabut License - see the LICENSE.md file for details
