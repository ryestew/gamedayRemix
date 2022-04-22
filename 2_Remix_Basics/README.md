# In this section, you'll go through the "compile and run" feature.

 - create a workspace.
 - switch to the `1_Storage.sol` file.
 - see the line `@custom:dev-run-script ./scripts/deploy_with_ethers.ts` in the contract's header.
 - this line states that the script `deploy_with_ethers.ts` will be run after the compilation finishes.
 - open the Solidity compiler and click on `Compile and Run` (you can also do Ctrl-Shift-S) (note that the `Compile` action will only compile without running any script). 
 - the compilation should start and the script run against the current selected environement.


 This feature allows you to run a script right after the compilation succeed, it aims to reduce the time spending
 on manually deploying contracts and settings them up in a desired state. Alternatively it's also possible to run mocha unit testing files.
