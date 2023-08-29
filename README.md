# ZK SNARK Circuit Designer
The primary objective of this project is to design and implement a logical gate circuit using the Circom programming language. Furthermore, it aims to showcase the capabilities of Zero-Knowledge Succinct Non-Interactive Argument of Knowledge (ZK-SNARK) proofs in verifying the knowledge of specific inputs that result in a particular output.

For the successful completion of this project, the following key steps will be undertaken:

### Circuit Implementation: 
Develop an accurate and functional logical gate circuit using the Circom programming language.

### Circuit Compilation: 
Compile the circuit, resulting in the generation of essential circuit intermediaries.

### ZK-SNARK Proof Generation: 
Create a ZK-SNARK proof utilizing the specified input values, namely A=0 and B=1.

### Solidity Verifier Contract Deployment: 
Deploy a Solidity-based verifier contract onto the Sepolia or Mumbai Testnet.

### Proof Verification: 
Execute the verifyProof() function present in the deployed verifier contract and assert the correctness of the output as true.

# Getting Started
To expedite the project initiation process, the subsequent steps are recommended:

Dependency Installation: Start by installing all required dependencies using the npm i command.

Circuit Compilation: Compile the circuit effortlessly by executing the command npx hardhat circom. The outcome will be an "out" directory containing circuit intermediaries alongside the CustomCircuitVerifier.sol contract.

# Proof Generation and Deployment
Execute the script npx hardhat run scripts/deploy.ts to seamlessly carry out the following actions:

# Deploy the CustomCircuitVerifier.sol contract.
Generate a proof using circuit intermediaries via the generateProof() function.
Formulate calldata using the generateCallData() function.
Utilize the calldata to invoke verifyProof() on the verifier contract.
# Configuration Considerations
Each distinct circuit resides within its own directory. At the topmost level of this directory, you'll find the circom circuit itself, as well as the input values. Following successful compilation, the "out" directory will be automatically created. This directory serves as the repository for compiled outputs, keys, and proofs. It's noteworthy that the Powers of Tau file is sourced from the Polygon Hermez ceremony, streamlining the process by obviating the necessity for a new ceremony.

The verifier contracts are auto-generated and prefixed according to the corresponding circuit's name.

# Deployment and Verification
To deploy the project onto the Mumbai Testnet, execute the command:
npx hardhat run scripts/deploy.ts --network mumbai

Subsequently, verify the transaction's success and confirm fulfillment on the Mumbai PolygonScan using the provided contract address.

# About the Author
Sourav Kashyap
