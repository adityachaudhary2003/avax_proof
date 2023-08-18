## Creating A Token.

The program provides a straightforward custom token named "MyToken" that was created using Solidity on the Ethereum blockchain. Tokens may be created and destroyed, and their overall supply and individual balances may be monitored. The programme makes sure that token holders have enough balance before conducting any burning operations by having the capacity to mint new tokens and burn current ones. This agreement may be freely used and distributed if it complies with the MIT licence. In general, it offers a simple and convenient framework for developing and administering unique tokens on the Ethereum network, providing a dependable answer for token tracking and granting.


## Description.

Solidity code for "MyToken" created for the Ethereum blockchain. Public variables in the contract are used to hold the token's name, acronym, and total supply as well as other important information. To efficiently maintain and manage ownership, it makes use of a mapping called "tokenHolders" that links Ethereum addresses with the corresponding token balances. The "mint" and "burn" capabilities are the program's two main features. The "mint" function enables the production of new tokens, expanding the available supply, and updating the recipient address's balance.The "burn" function makes it easier to destroy tokens, which lowers the overall supply and subtracts the desired sum from the balance of the token holder. It's significant that the "burn" function includes a check to make sure the token holder has enough money in their account to cover the requested burn amount. With these features, the contract offers a complete answer for managing balances and creating and destroying tokens in a safe and decentralised blockchain ecosystem.


## Getting started.


pragma solidity 0.8.17;

contract MyToken {

    string public tokenName = "META";
    string public tokenAbbrv ="MTA";
    uint public totalSupply = 0;

    mapping (address => uint ) public balances;

    function mint(address _address,uint _values) public{
        totalSupply+=_values;
        balances[_address]+=_values;
    }

    function burn (address _address,uint _values) public{
        if(balances[_address] >= _values){
        totalSupply -= _values;
        balances[_address] -= _values;

        }
        
    }
}




## Executing program

Deploy the program, then use the default address provided. Then paste the copied address to mint and add some value After that check the Balance. We can also burn token by using burn. Again, add the copied default address Add the value that you want to burn Burn the token Check the balance.



