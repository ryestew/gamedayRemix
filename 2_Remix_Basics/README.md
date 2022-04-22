# In this section, you'll go through the "compile and run" feature.

 - Create a workspace.
 - Switch to the `1_Storage.sol` file.
 - See the line `@custom:dev-run-script ./scripts/deploy_with_ethers.ts` in the contract's header.
 - This line states that the script `deploy_with_ethers.ts` will be run after the compilation finishes.
 - Open the Solidity compiler and click on `Compile and Run` (you can also do Ctrl-Shift-S) (note that the `Compile` action will only compile without running any script). 
 - The compilation should start and the script run against the current selected environement.


 This feature allows you to run a script right after the compilation succeed, it aims to reduce the time spending
 on manually deploying contracts and settings them up in a desired state. Alternatively it's also possible to run mocha unit testing files.

 # Use layer 2 - Optimism

 - You need to have metamask installed for this section. Use this for the step by step: https://metamask.zendesk.com/hc/en-us/articles/360043227612-How-to-add-a-custom-network-RPC and https://metamask.zendesk.com/hc/en-us/articles/4415758352667-Network-profile-Optimism for the chain information.
 - Switch to the Optimism network in metamask
 - Then it's a typical deployment: compile, switch to the `Run and Deploy`, and hit Deploy.
 - Your contract is deployed to Optimism!
 
