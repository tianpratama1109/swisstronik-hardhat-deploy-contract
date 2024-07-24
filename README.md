# Swisstronik Tesnet Techinal Task 1

## Steps

### 1. Clone Repository

```bash
git clone https://github.com/tianpratama1109/swisstronik-hardhat-deploy-contract.git
```

```
cd hardhat-deploy-contract
```

### 2. Install Dependency

```bash
npm install
```

### 3. Set Up .env File

Create a .env file in the root of the project with the following content:

```bash
PRIVATE_KEY="your private key"
```

### 4. Create Smart Contract

- Open the contract folder
- Create a file named Hello_swtr.sol
- Copy and paste the following code into the file:

```
/// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.19;

//This contract is only intended for testing purposes

contract Swisstronik {
    string private message;

    /**
     * @dev Constructor is used to set the initial message for the contract
     * @param _message the message to associate with the message variable.
     */
    constructor(string memory _message) payable{
        message = _message;
    }

    /**
     * @dev setMessage() updates the stored message in the contract
     * @param _message the new message to replace the existing one
     */
    function setMessage(string memory _message) public {
        message = _message;
    }

    /**
     * @dev getMessage() retrieves the currently stored message in the contract
     * @return The message associated with the contract
     */
    function getMessage() public view returns(string memory){
        return message;
    }
}
```

### 5. Compile the Smart Contract

```bash
npm run compile
```

### 6.  Deploy the Smart Contract

```bash
npm run deploy
```

### 7. Retrieve the Message

```bash
npm run get-message
```

### 8. Update the Message

```bash
npm run set-message
```

### 9. Finsihed

- Open the deployed-address.ts file (located in the utils folder)
- Copy the address and paste it into the testnet dashboard
- Push the project to your GitHub repository and paste the repository link into the testnet dashboard
