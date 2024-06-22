Project Title

ETH PROOF: Beginner EVM Course final project

Description
First, I built a contract called MyToken for the first task. I defined and assigned values to three public variables in this contract: tokenName, tokenAbbreviations, and totalSupply. The token's name is recorded in the tokenName field, its abbreviation is contained in the tokenAbbreviations field, and the totalSupply field tracks the total balance. I then constructed a mapping named balance that maps an unsigned integer to each address. Next, I created a mint function that takes two parameters: an unsigned integer called "value" and an address called "adr." The input address's balance and total supply are increased by the given amount using this function. Finally, using the same parameters as the mint function, I created a burn function.This burn function determines whether the amount to be subtracted is less than the address's balance. The designated amount is subtracted from the address's balance as well as the total supply if the condition is met.


Getting Started

Go to https://remix.ethereum.org/
Create a new file with file extension as .sol and compile the program.

File name can be xyz.sol

Author

Anuj
