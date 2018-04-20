# Ethereum-metacoin
testing metacoin

Errors encountered:
- truffle migrate
  ```
  $ truffle migrate
  Could not connect to your Ethereum client. Please check that your Ethereum client:
      - is running
      - is accepting RPC connections (i.e., "--rpc" option is used in geth)
      - is accessible over the network
      - is properly configured in your Truffle configuration file (truffle.js)
  ```
    - Solution:
        Change truffle.js file with following port
        ````
        module.exports = {
          networks: {
            development: {
              host: "127.0.0.1",
              port: 7545,
              network_id: "*" // Match any network id
            }
          }
        };

        ````
