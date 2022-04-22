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
 - Confirm the transaction in Metamask.
 - Your contract is deployed to Optimism!

 # Use the debugger and proxy contract

 We are going here to deploy a contract, its proxy and see what is the issue with it.
 
 - Load this URL https://remix.ethereum.org/#code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IE1JVApwcmFnbWEgc29saWRpdHkgXjAuOC4wOwoKLy8gaW1wb3J0ICJAb3BlbnplcHBlbGluL2NvbnRyYWN0cy9tYXRoL1NhZmVNYXRoLnNvbCI7CmltcG9ydCAiQG9wZW56ZXBwZWxpbi9jb250cmFjdHMvcHJveHkvRVJDMTk2Ny9FUkMxOTY3UHJveHkuc29sIjsKCmNvbnRyYWN0IFB1enpsZVByb3h5IGlzIEVSQzE5NjdQcm94eSB7CiAgICBhZGRyZXNzIHB1YmxpYyBwZW5kaW5nQWRtaW47CiAgICBhZGRyZXNzIHB1YmxpYyBhZG1pbjsKCiAgICBjb25zdHJ1Y3RvcihhZGRyZXNzIF9hZG1pbiwgYWRkcmVzcyBfaW1wbGVtZW50YXRpb24sIGJ5dGVzIG1lbW9yeSBfaW5pdERhdGEpIEVSQzE5NjdQcm94eShfaW1wbGVtZW50YXRpb24sIF9pbml0RGF0YSkgcHVibGljIHsKICAgICAgICBhZG1pbiA9IF9hZG1pbjsKICAgIH0KCiAgICBtb2RpZmllciBvbmx5QWRtaW4gewogICAgICByZXF1aXJlKG1zZy5zZW5kZXIgPT0gYWRtaW4sICJDYWxsZXIgaXMgbm90IHRoZSBhZG1pbiIpOwogICAgICBfOwogICAgfQoKICAgIGZ1bmN0aW9uIHByb3Bvc2VOZXdBZG1pbihhZGRyZXNzIF9uZXdBZG1pbikgZXh0ZXJuYWwgewogICAgICAgIHBlbmRpbmdBZG1pbiA9IF9uZXdBZG1pbjsKICAgIH0KCiAgICBmdW5jdGlvbiBhcHByb3ZlTmV3QWRtaW4oYWRkcmVzcyBfZXhwZWN0ZWRBZG1pbikgZXh0ZXJuYWwgb25seUFkbWluIHsKICAgICAgICByZXF1aXJlKHBlbmRpbmdBZG1pbiA9PSBfZXhwZWN0ZWRBZG1pbiwgIkV4cGVjdGVkIG5ldyBhZG1pbiBieSB0aGUgY3VycmVudCBhZG1pbiBpcyBub3QgdGhlIHBlbmRpbmcgYWRtaW4iKTsKICAgICAgICBhZG1pbiA9IHBlbmRpbmdBZG1pbjsKICAgIH0KCiAgICBmdW5jdGlvbiB1cGdyYWRlVG8oYWRkcmVzcyBfbmV3SW1wbGVtZW50YXRpb24pIGV4dGVybmFsIG9ubHlBZG1pbiB7CiAgICAgICAgX3VwZ3JhZGVUbyhfbmV3SW1wbGVtZW50YXRpb24pOwogICAgfQp9Cgpjb250cmFjdCBQdXp6bGVXYWxsZXQgewogICAgYWRkcmVzcyBwdWJsaWMgb3duZXI7CiAgICB1aW50MjU2IHB1YmxpYyBtYXhCYWxhbmNlOwogICAgbWFwcGluZyhhZGRyZXNzID0+IGJvb2wpIHB1YmxpYyB3aGl0ZWxpc3RlZDsKICAgIG1hcHBpbmcoYWRkcmVzcyA9PiB1aW50MjU2KSBwdWJsaWMgYmFsYW5jZXM7CgogICAgZnVuY3Rpb24gaW5pdCh1aW50MjU2IF9tYXhCYWxhbmNlKSBwdWJsaWMgewogICAgICAgIHJlcXVpcmUobWF4QmFsYW5jZSA9PSAwLCAiQWxyZWFkeSBpbml0aWFsaXplZCIpOwogICAgICAgIG1heEJhbGFuY2UgPSBfbWF4QmFsYW5jZTsKICAgICAgICBvd25lciA9IG1zZy5zZW5kZXI7CiAgICB9CgogICAgbW9kaWZpZXIgb25seVdoaXRlbGlzdGVkIHsKICAgICAgICByZXF1aXJlKHdoaXRlbGlzdGVkW21zZy5zZW5kZXJdLCAiTm90IHdoaXRlbGlzdGVkIik7CiAgICAgICAgXzsKICAgIH0KCiAgICBmdW5jdGlvbiBzZXRNYXhCYWxhbmNlKHVpbnQyNTYgX21heEJhbGFuY2UpIGV4dGVybmFsIG9ubHlXaGl0ZWxpc3RlZCB7CiAgICAgIHJlcXVpcmUoYWRkcmVzcyh0aGlzKS5iYWxhbmNlID09IDAsICJDb250cmFjdCBiYWxhbmNlIGlzIG5vdCAwIik7CiAgICAgIG1heEJhbGFuY2UgPSBfbWF4QmFsYW5jZTsKICAgIH0KCiAgICBmdW5jdGlvbiBhZGRUb1doaXRlbGlzdChhZGRyZXNzIGFkZHIpIGV4dGVybmFsIHsKICAgICAgICByZXF1aXJlKG1zZy5zZW5kZXIgPT0gb3duZXIsICJOb3QgdGhlIG93bmVyIik7CiAgICAgICAgd2hpdGVsaXN0ZWRbYWRkcl0gPSB0cnVlOwogICAgfQoKICAgIGZ1bmN0aW9uIGRlcG9zaXQoKSBleHRlcm5hbCBwYXlhYmxlIG9ubHlXaGl0ZWxpc3RlZCB7CiAgICAgIHJlcXVpcmUoYWRkcmVzcyh0aGlzKS5iYWxhbmNlIDw9IG1heEJhbGFuY2UsICJNYXggYmFsYW5jZSByZWFjaGVkIik7CiAgICAgIGJhbGFuY2VzW21zZy5zZW5kZXJdID0gYmFsYW5jZXNbbXNnLnNlbmRlcl0gKyBtc2cudmFsdWU7CiAgICB9CgogICAgZnVuY3Rpb24gZXhlY3V0ZShhZGRyZXNzIHRvLCB1aW50MjU2IHZhbHVlLCBieXRlcyBjYWxsZGF0YSBkYXRhKSBleHRlcm5hbCBwYXlhYmxlIG9ubHlXaGl0ZWxpc3RlZCB7CiAgICAgICAgcmVxdWlyZShiYWxhbmNlc1ttc2cuc2VuZGVyXSA+PSB2YWx1ZSwgIkluc3VmZmljaWVudCBiYWxhbmNlIik7CiAgICAgICAgYmFsYW5jZXNbbXNnLnNlbmRlcl0gPSBiYWxhbmNlc1ttc2cuc2VuZGVyXSAtIHZhbHVlOwogICAgICAgIChib29sIHN1Y2Nlc3MsICkgPSB0by5jYWxseyB2YWx1ZTogdmFsdWUgfShkYXRhKTsKICAgICAgICByZXF1aXJlKHN1Y2Nlc3MsICJFeGVjdXRpb24gZmFpbGVkIik7CiAgICB9CgogICAgZnVuY3Rpb24gbXVsdGljYWxsKGJ5dGVzW10gY2FsbGRhdGEgZGF0YSkgZXh0ZXJuYWwgcGF5YWJsZSBvbmx5V2hpdGVsaXN0ZWQgewogICAgICAgIGJvb2wgZGVwb3NpdENhbGxlZCA9IGZhbHNlOwogICAgICAgIGZvciAodWludDI1NiBpID0gMDsgaSA8IGRhdGEubGVuZ3RoOyBpKyspIHsKICAgICAgICAgICAgYnl0ZXMgbWVtb3J5IF9kYXRhID0gZGF0YVtpXTsKICAgICAgICAgICAgYnl0ZXM0IHNlbGVjdG9yOwogICAgICAgICAgICBhc3NlbWJseSB7CiAgICAgICAgICAgICAgICBzZWxlY3RvciA6PSBtbG9hZChhZGQoX2RhdGEsIDMyKSkKICAgICAgICAgICAgfQogICAgICAgICAgICBpZiAoc2VsZWN0b3IgPT0gdGhpcy5kZXBvc2l0LnNlbGVjdG9yKSB7CiAgICAgICAgICAgICAgICByZXF1aXJlKCFkZXBvc2l0Q2FsbGVkLCAiRGVwb3NpdCBjYW4gb25seSBiZSBjYWxsZWQgb25jZSIpOwogICAgICAgICAgICAgICAgLy8gUHJvdGVjdCBhZ2FpbnN0IHJldXNpbmcgbXNnLnZhbHVlCiAgICAgICAgICAgICAgICBkZXBvc2l0Q2FsbGVkID0gdHJ1ZTsKICAgICAgICAgICAgfQogICAgICAgICAgICAoYm9vbCBzdWNjZXNzLCApID0gYWRkcmVzcyh0aGlzKS5kZWxlZ2F0ZWNhbGwoZGF0YVtpXSk7CiAgICAgICAgICAgIHJlcXVpcmUoc3VjY2VzcywgIkVycm9yIHdoaWxlIGRlbGVnYXRpbmcgY2FsbCIpOwogICAgICAgIH0KICAgIH0KfQo&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.7+commit.e28d00a7.js

  - This will load the PuzzleProxy (you can also find it there https://ethernaut.openzeppelin.com/level/0xe13a4a46C346154C41360AAe7f070943F67743c9 )

  - Compile this file and Deploy `PuzzleWallet`, this is the implementation contract (the code that will be run).
  - Deploy `PuzzleProxy`, it requires 3 parameters:

        - the owner (your address)

        - the implementation contract. This is the address of `Puzzle Wallet`.
        
        - the init code. 
        This give the proxy all the necessary data for the proxy to initiate the implementation contract. In our case, this should be
        0xb7b0422d which is the signature of the `init` function, followed by the actual parameters. 

        There is only one parameter: `_maxBalance` which we can set to 1: 0x0000000000000000000000000000000000000000000000000000000000000001.

        So 0xb7b0422d0000000000000000000000000000000000000000000000000000000000000001 allows the proxy to call the `init` function with 1 as first and only parameter.

  - Now Ok: these contracts are completely bugged. In short, call the `proposeNewAdmin` from the proxy using another address. it updates the `pendingAdmin`, that's fine. But look at how the implementation will interpret these updates: 
      For the implementation, you were directly updating the `owner` property!
  - From the terminal, click on `Debug` and you can check that `pendingAdmin` is updated.
  - In order to fix we must ensure that the place in the storage where the address of the implementation contract is stored will never collide with a state variable in the implementation contract, and here is the solution: https://eips.ethereum.org/EIPS/eip-1967
  - Another issue is that the `init` function is not protected and can be called many times, which is a huge security issue. A solution for that is provided by the OpenZeppelin stack: https://github.com/OpenZeppelin/openzeppelin-contracts-upgradeable/blob/master/contracts/proxy/utils/Initializable.sol#L78
  



