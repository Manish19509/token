#ETH-Proof Assessment - Getting Started with Solidity

In this, I will be sharing my learnings done by this Metacrafter course assessment.

## Description

A token called Manish (Man) with an initial total supply of 0 tokens is represented by this Solidity contract named ManishToken. To maintain the integrity of the token balance, it permits minting new tokens to a designated address and burning existing tokens from a specified address.

## Getting Started
In this assessment, I have used remix IDE[https://remix.ethereum.org/]

### Executing program

* written code
![image](https://github.com/Manish19509/token/assets/137030058/98902414-808d-484c-a33a-ee20c8269e9e)

* Compile the code
* ![image](https://github.com/Manish19509/token/assets/137030058/6eb7894e-f714-41f6-b7ec-d8d6a2c46808)

* make the compiler version the same as mentioned in the program.
* Go to the deploy and transact section and click on transact after selecting the account.
* By clicking on the transact we will be able to see the deployed contracts.
* By coping account address, adding it to burn and mint and puting value the total supply will change according to the code.
* ![image](https://github.com/Manish19509/token/assets/137030058/e0b3512a-e225-46df-9fa5-852870c7f033)
 
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
/*   REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of xthe mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/
contract ManishToken {
    // public variables here
    //Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    //string public
    string public token_Name ="Manish" ;
    string public token_Abbreviation = "Man";
    uint public totalSupp1y = 0; //unsigned integer
    // mapping variable here
    // Your contract will have a mapping of addresses to balances (address => uint)
    //defines a public state variable named tokenbalances that mapping address to unit(unsigned integer values) ,make it public
    mapping(address =>uint) public tokenbalances;

    // mint function
    function mint (address _address, uint _value) public {
    totalSupp1y += _value;
    tokenbalances [_address] += _value;
    }
    // burn function
    function burn (address _address, uint _value) public {
    if (tokenbalances[_address] >= _value){
    totalSupp1y -= _value;
    tokenbalances[_address]-= _value;
    }}}
```

## Authors

Manish Kumar gmail - manishkeshri19509@gmail.com




## License

This project is licensed under the MIT License
