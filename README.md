# ETH PROOF: Beginner EVM Course final project
This contract manages a custom token. It keeps track of balances for each user and the total supply. It allows creating new tokens (minting) for an address and destroying existing tokens (burning) from the sender's account.
## Description
The MyToken contract implements basic functionalities to handle a custom token on the Ethereum blockchain. It includes:

1. Stores token details (name, symbol, total supply) publicly.

2. Tracks balances per address using a mapping.

3. Mints new tokens for an address with mint.

4. Burns tokens from an address (with balance check) with burn.

This contract serves as a simple introduction to creating and managing custom tokens using Solidity.

## Getting Started

- Run on Remix IDE: Use Remix for online execution.
- Create a new Solidity file: Click "+" in the left sidebar, save as .sol (e.g., MyToken.sol).
- Paste the code: Copy and paste your Solidity code into the file.

---
    pragma solidity ^0.8.18;  
 
    contract MyToken 
    {
    string public tokenName = "Coin";
    string public tokenAbbreviation="cn";
    uint public totelSupply=0;
    mapping(address => uint) public balances;
        function mint(address adr,uint value) public {
        totelSupply+=value;
        balances[adr]+=value;
            }
    function burn (address adr,uint value) public {
        if(balances[adr]>=value){
        totelSupply-=value;
        balances[adr]-=value;   
            }
            } }

- Gettin' it ready to run: Head over to the "Solidity Compiler" tab on the left. Make sure the "Compiler" version is set to something that works with your code (like 0.8.25). Then, hit that "Compile MyToken.sol" button!

- Deployment time!: Now switch to the "Deploy & Run Transactions" tab. Find MyToken in the dropdown menu and click "Deploy" to unleash your contract to the world (well, a virtual world at least).

- Let's play!: Remix provides a cool interface to interact with your contract. Use it to call those mint and burn functions. Just fill in the info they need and hit the buttons to make it happen!
## Help
If you encounter any issues, ensure the following:

- The Solidity compiler version is set correctly.
- The address used in function calls is valid.
- The balance of the address is sufficient for burning tokens.
For additional help, use the Remix documentation or community forums.

## Author
Anuj

anujgill240@gmail.com

## License
This project is licensed under the MIT License.
