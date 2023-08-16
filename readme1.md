Certainly! You can develop and audit Solidity projects offline, especially if you're concerned about security or simply don't want an internet-dependent workflow. Here's a guide on how to set up and work on your Solidity projects offline:

### 1. **Offline Development**:

1. **Install Tools Locally**:
   - **Solidity Compiler (solc)**: Download and install the Solidity compiler locally. This way, you can compile your contracts offline.
   - **Remix Desktop**: You mentioned Remix 1.3.6, which I assume is the Remix Desktop version. It can work offline and offers a similar experience to the web version.

2. **Code Editing**: 
   - Use Remix Desktop or any text editor/IDE of your choice. Popular choices include Visual Studio Code with the Solidity extension.

3. **Compile with solc**: If you're not using Remix Desktop, you can compile your contracts using the command line. Navigate to your project directory and use:
   ```bash
   solc --bin --abi YourContract.sol
   ```
   This will generate the binary (bytecode) and ABI for your contract.

### 2. **Offline Testing**:

1. **Ganache**: Ganache is a personal blockchain for Ethereum development that you can use to deploy contracts, develop your applications, and run tests. It runs on your local machine, allowing for offline development.
   - Download and install Ganache.
   - Run it to have a local Ethereum instance with pre-funded accounts.

2. **Truffle or Hardhat**: These are development frameworks for Ethereum that allow you to write and test smart contracts.
   - Setup and initialize a project.
   - Write migrations to deploy your contracts to the local Ganache instance.
   - Write tests in Solidity or JavaScript.
   - Run the tests against the Ganache instance.

### 3. **Offline Auditing**:

1. **Static Analysis**: Remix has a static analysis tool you can run offline with the desktop version.
   
2. **Mythril**: Mythril is a security analysis tool for Ethereum smart contracts. You can install it locally and use it to detect common Solidity vulnerabilities.

3. **Manual Code Review**: Often the most effective audit is a thorough manual review. Familiarize yourself with common Solidity vulnerabilities, best practices, and ensure your code adheres to them.

### 4. **Other Tools**: 

1. **solhint**: This is a linter for Solidity to enforce style and security rules.

2. **Slither**: This is a static analysis tool for Solidity, designed to find vulnerabilities, enhance the code's quality, and ensure adherence to best practices.

Remember, while offline development and auditing can offer a secure environment, it's essential to keep your tools updated. Security tools especially frequently receive updates to detect new vulnerabilities or enhance existing checks. Periodically connect to the internet to update your tools, but always make sure you're downloading from official or trusted sources.