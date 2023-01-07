# ICO

- There should be a max of 10,000 CD tokens.
- Every Crypto Dev NFT holder should get 10 tokens for free but they would have to pay the gas fees.
- The price of one CD at the time of ICO should be 0.001 ether.
- There should be a website that users can visit for the ICO.

## Setup Hardhat

```bash
cd hardhat-tutorial
# init hardhat
npx hardhat
npm install @openzeppelin/contracts
# remove boilerplate contract to prevent errors
rm contracts/Lock.sol
# create interface contracts
touch contracts/ICryptoDevs.sol
code contracts/ICryptoDevs.sol
# create token contract
touch contracts/CryptoDevToken.sol
code contracts/CryptoDevToken.sol
# set environment variables
npm install dotenv
touch .env.example
echo 'QUICKNODE_HTTP_URL=""' >> .env.example
echo 'PRIVATE_KEY=""' >> .env.example
cp .env.example .env
# set nft contract address
mkdir constants
touch constants/index.js

code constants/index.js
code scripts/deploy.js
code hardhat.config.js


```

### update files then compile & deploys

```
npx hardhat compile
npx hardhat run scripts/deploy.js --network goerli
```
