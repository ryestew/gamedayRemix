# Interacting with Moonbeam's DemocracyInterface.sol 

In this section, you'll cast your vote for the most likely conspirator by interacting with DemocracyInterface.sol on Moonbase Alpha, the public testnet for Moonbeam.

## Tasks

1. Add Moonbase Alpha to MetaMask via the Connect MetaMask Button at the top of the [Moonbeam Docs Site](https://docs.moonbeam.network/) or via [Chainlist](https://chainlist.org/)
2. Request faucet funds in the #Moonbase-Faucet channel of the [Moonbeam Discord](http://discord.gg/moonbeam). The #Moonbase-Faucet is located under the Miscellaneous folder.
3. Copy [DemocracyInterface.sol](https://github.com/PureStake/moonbeam/blob/master/precompiles/pallet-democracy/DemocracyInterface.sol) into a new file named DemocracyInterface.sol in Remix. Compile the Contract.
4. Make sure your MetaMask is on the Moonbase Alpha Network. On the Deploy & Run Tab in Remix, change the environment to Injected Web3, and immediately below you that should see `Custom (1287) Network`. If you don't see that, switch your MetaMask to the Moonbase Alpha network and refresh the page.
5. Instead of deploying a contract, enter the address of the democracy precompile `0x0000000000000000000000000000000000000803` and press “At Address”.
6. Expand the deployed contract, and find the `standard_vote` method.
7. Head to [Polkassembly](https://moonbase.polkassembly.network/) and find the referendum index of the most likely conspirator that you want to cast your vote for. Input the referendum index as the first parameter. 
8. Input 1 in the `aye` field (1 is a vote for YES)
9. Enter a `vote_amount` that is less than the total number of DEV tokens you have - need to save some for gas. If you have 5 DEV tokens, the max vote amount you should submit is 4.99 DEV for example. 
10. Based on how confident you are in the culprit, enter a conviction between 0-6 inclusive that represents the desired lock period for the tokens committed to the vote, where 0 represents minimal conviction with no lock period and 6 represents the maximum conviction and lock period (32 days in Moonbase Alpha). A conviction of 0 means your vote weight is 10% of your tokens locked, whereas convictions 1-6 are a multiplication factor - a conviction of 6 for example means your vote is weight at 6 times your lock balance.

## Observing the Results 
You can view the results on [Polkassembly](https://moonbase.polkassembly.network/). You are free to vote for multiple culprits if you are uncertain. 

## Resources
You can view a complete guide to the [DemocracyInterface.sol on the Moonbeam Docs Site](https://docs.moonbeam.network/builders/build/canonical-contracts/precompiles/democracy/).  
