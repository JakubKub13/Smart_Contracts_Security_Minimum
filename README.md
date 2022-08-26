Two most common attacks:
- Reentrancy
- Oracle Manipulation

RUN STATIC ANALYSIS on given contracts
1. SLITHER  -> Trail of Bits team one of the best opensource tools to audit SC
- we need to install python first in order to use Slither
- we need to install solc-select package  -> pip3 install solc-select
--> solc-select use 0.8.7 (use for solidity version 0.8.7)
- after we run -> pip3 install slither-analyzer 
- We check if everything was successful -> slither --help
- We can use Slither to run it on our contracts folder by typing -> npm run slither
Slither will not catch every vulnerability but it catches a lot of major ones


RUN MANUAL ANALYSIS on given contracts
We walk through the code ourselves and run slower tools (echidna, manticore, symbolic execution, MythX) 
Symbolic execution = simulation of transaction execution on blockchain
Fuzz testing is automated software testing that involves providing invalid, unexpected or random data inputs to cp program.
1. We write our Fuzz test in SOLIDITY not in JS
- Download package -> eth-security-toolbox
- 1. To work with the tool we need to install Docker
- 2. After we have Docker installed we can run the eth-security-toolbox by pulling it down from Docker equivalent of GitHub
Docker commands: 
    - npm run toolbox
After successfully installed and configurated docker we run command:
    - echidna-test /src/contracts/test/VaultFuzzTest.sol --contract VaultFuzzTest --config /src/contracts/test/config.yaml


Before deployment of contracts we have to ALWAYS:
    - Run Slither
    - Look MANUALLY for Reentrancy attack or Oracle Manipulation# Smart_Contract_Security_Minimum
# Smart_Contracts_Security_Minimum
# Smart_Contracts_Security_Minimum
