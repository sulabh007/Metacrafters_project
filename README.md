# Create a Token

This project will walk you through the process of creating a token using Solidity that demonstrates the minting and burning of token

## Description

his program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has functions that perform Burning and minting of token . This program serves as a simple and straightforward introduction to token creation, and can be used as a stepping stone for more complex projects in the future.

## Getting Started


### Executing program

* The contract has public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
* it has a mapping of addresses to balances (address => uint)
* it hasa a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the address by that amount.
* it has a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the address.
* Lastly, your burn function should have conditionals to make sure the balance of account is greater than or equal to the amount that is supposed to be burned.
```
function mint(address _address, uint _val) public {
        total_supply+=_val;
        balances[_address]+=_val;
    }
    // burn function
    function burn(address _address, uint _val) public {
        
        if(_val<=balances[_address]){
            total_supply-=_val;
            balances[_address]-=_val;
        }
        

    }
```


## Authors

Contributors names and contact info

* Sulabh Jha 
* [@SulabhJha](https://www.linkedin.com/in/sulabh-jha-6709621a0/)


## License

This project is licensed under the Sulabh Jha License - see the LICENSE.md file for details
