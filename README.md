MyToken - A Simple Token Contract

Description:
The MyToken project is a basic implementation of a token contract called MyToken. The contract allows for the creation and management of tokens on the Ethereum blockchain. It includes functions for minting and burning tokens. The contract keeps track of the total token supply and individual balances for each address.

Getting Started:

Installing:
Since this is a smart contract written in Solidity, there is no need for installation in the traditional sense. You would need to have a development environment with a Solidity compiler (e.g., Remix, Truffle) set up to compile and deploy the contract.

Executing program:

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Token.sol). Copy and paste the following code into the file

     contract MyToken {
    // public variables here
    string public TokenName = "META";
    string public TokenAbbrv = "MTA";
    uint public totalSupply = 0;
    
    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
    
    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
    }

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Mytoken" contract from the dropdown menu, and then click on the "Deploy" button.



