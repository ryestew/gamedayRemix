# In this section, you'll go through a lot of Remix tools.

## Tasks

1. Load this URL to see a contract of a  Dutch auction (contract from Solidity by example).  This url loads a base64 encoded text of a solidity file into the Remix editor. 

    https://remix.ethereum.org/?#code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IE1JVApwcmFnbWEgc29saWRpdHkgXjAuOC4xMDsKCmludGVyZmFjZSBJRVJDNzIxIHsKICAgIGZ1bmN0aW9uIHRyYW5zZmVyRnJvbSgKICAgICAgICBhZGRyZXNzIF9mcm9tLAogICAgICAgIGFkZHJlc3MgX3RvLAogICAgICAgIHVpbnQgX25mdElkCiAgICApIGV4dGVybmFsOwp9Cgpjb250cmFjdCBEdXRjaEF1Y3Rpb24gewogICAgdWludCBwcml2YXRlIGNvbnN0YW50IERVUkFUSU9OID0gNyBkYXlzOwoKICAgIElFUkM3MjEgcHVibGljIGltbXV0YWJsZSBuZnQ7CiAgICB1aW50IHB1YmxpYyBpbW11dGFibGUgbmZ0SWQ7CgogICAgYWRkcmVzcyBwYXlhYmxlIHB1YmxpYyBpbW11dGFibGUgc2VsbGVyOwogICAgdWludCBwdWJsaWMgaW1tdXRhYmxlIHN0YXJ0aW5nUHJpY2U7CiAgICB1aW50IHB1YmxpYyBpbW11dGFibGUgc3RhcnRBdDsKICAgIHVpbnQgcHVibGljIGltbXV0YWJsZSBleHBpcmVzQXQ7CiAgICB1aW50IHB1YmxpYyBpbW11dGFibGUgZGlzY291bnRSYXRlOwoKICAgIGNvbnN0cnVjdG9yKAogICAgICAgIHVpbnQgX3N0YXJ0aW5nUHJpY2UsCiAgICAgICAgdWludCBfZGlzY291bnRSYXRlLAogICAgICAgIGFkZHJlc3MgX25mdCwKICAgICAgICB1aW50IF9uZnRJZAogICAgKSB7CiAgICAgICAgc2VsbGVyID0gcGF5YWJsZShtc2cuc2VuZGVyKTsKICAgICAgICBzdGFydGluZ1ByaWNlID0gX3N0YXJ0aW5nUHJpY2U7CiAgICAgICAgc3RhcnRBdCA9IGJsb2NrLnRpbWVzdGFtcDsKICAgICAgICBleHBpcmVzQXQgPSBibG9jay50aW1lc3RhbXAgKyBEVVJBVElPTjsKICAgICAgICBkaXNjb3VudFJhdGUgPSBfZGlzY291bnRSYXRlOwoKICAgICAgICByZXF1aXJlKF9zdGFydGluZ1ByaWNlID49IF9kaXNjb3VudFJhdGUgKiBEVVJBVElPTiwgInN0YXJ0aW5nIHByaWNlIDwgbWluIik7CgogICAgICAgIG5mdCA9IElFUkM3MjEoX25mdCk7CiAgICAgICAgbmZ0SWQgPSBfbmZ0SWQ7CiAgICB9CgogICAgZnVuY3Rpb24gZ2V0UHJpY2UoKSBwdWJsaWMgdmlldyByZXR1cm5zICh1aW50KSB7CiAgICAgICAgdWludCB0aW1lRWxhcHNlZCA9IGJsb2NrLnRpbWVzdGFtcCAtIHN0YXJ0QXQ7CiAgICAgICAgdWludCBkaXNjb3VudCA9IGRpc2NvdW50UmF0ZSAqIHRpbWVFbGFwc2VkOwogICAgICAgIHJldHVybiBzdGFydGluZ1ByaWNlIC0gZGlzY291bnQ7CiAgICB9CgogICAgZnVuY3Rpb24gYnV5KCkgZXh0ZXJuYWwgcGF5YWJsZSB7CiAgICAgICAgcmVxdWlyZShibG9jay50aW1lc3RhbXAgPCBleHBpcmVzQXQsICJhdWN0aW9uIGV4cGlyZWQiKTsKCiAgICAgICAgdWludCBwcmljZSA9IGdldFByaWNlKCk7CiAgICAgICAgcmVxdWlyZShtc2cudmFsdWUgPj0gcHJpY2UsICJFVEggPCBwcmljZSIpOwoKICAgICAgICBuZnQudHJhbnNmZXJGcm9tKHNlbGxlciwgbXNnLnNlbmRlciwgbmZ0SWQpOwogICAgICAgIHVpbnQgcmVmdW5kID0gbXNnLnZhbHVlIC0gcHJpY2U7CiAgICAgICAgaWYgKHJlZnVuZCA+IDApIHsKICAgICAgICAgICAgcGF5YWJsZShtc2cuc2VuZGVyKS50cmFuc2ZlcihyZWZ1bmQpOwogICAgICAgIH0KICAgICAgICBzZWxmZGVzdHJ1Y3Qoc2VsbGVyKTsKICAgIH0KfQo=

2. Publish it to a gist
    - hint: rt click on the file in the Files Explorer (if you have input your git credentials in the settings panel)

3. Clone this repo: Using DGIT clone this repo: https://github.com/ryestew/gamedayRemix.git
    - hint: use the dgit plugin

4. Compile using the clue in this tweet
https://twitter.com/EthereumRemix/status/1511901727389147136

5. Get the ABI (see the Solidity Compiler)

6. Make a new workspace. Load this GIST f: 

7. Using AtAddress access this contract deployed on this network and use this function to get the next clue - git address of a repo.

8. This contract is deployed on multiple testnets and optimism-kovan with the same address.

Extra Credit - how did we deploy to multiple nets with the same address?

9. Make this.sol the active file in the editor. 

10. Console.log: Add the import and do a console.log and add this on line XX and return the result you see in the console.

11. Export it to IPFS

12. Sign a message -use the IPFS hash as the message & put the Signature in the worksheet.

13. Go to Learneth and in the solidity basics class - go to step 7.2 and then to the sample .sol file.  Look on line 13 of loops.sol.  What is the last word on this line? 