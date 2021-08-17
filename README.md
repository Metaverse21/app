🏗 Scaffold-ETH - 🎟 Simple NFT Example
Build, mint, and send around your own ERC721!

🏃‍♀️ Quick Start
Required: Node plus Yarn and Git

git clone https://github.com/austintgriffith/scaffold-eth.git simple-nft-example
cd simple-nft-example
git checkout simple-nft-example
yarn install
yarn start
in a second terminal window:

cd simple-nft-example
yarn chain
in a third terminal window:

cd simple-nft-example
yarn deploy
📱 Open http://localhost:3000 to see the app

✏️ Edit the mint script mint.js in packages/hardhat/scripts and update the toAddress to your frontend address (wallet address in the top right or localhost:3000).

nft1

in a terminal window run the mint script:

yarn mint
nft2

👀 You should see your collectibles show up if you minted to the correct address:

nft3

👛 Open an incognito window and navigate to http://localhost:3000 (You'll notice it has a new wallet address).

⛽️ Grab some gas for each account using the faucet:

nft4

🎟 Send an NFT to the incognito window address:

nft5

🕵🏻‍♂️ Inspect the Debug Contracts tab to figure out what address is the owner of YourCollectible?

💼 Edit your deployment script deploy.js in packages/hardhat/scripts

🔏 Edit your smart contract YourCollectible.sol in packages/hardhat/contracts

📝 Edit your frontend App.jsx in packages/react-app/src

🔑 Create wallet links to your app with yarn wallet and yarn fundedwallet

⬇️ Installing a new package to your frontend? You need to cd packages/react-app and then yarn add PACKAGE

📡 Deploy NFT smart contract!
🛰 Ready to deploy to a testnet?

Change the defaultNetwork in packages/hardhat/hardhat.config.js

nft6

🔐 Generate a deploy account with yarn generate

nft7

👛 View your deployer address using yarn account (You'll need to fund this account. Hint: use an instant wallet to fund your account via QR code)

nft8

👨‍🎤 Deploy your NFT smart contract:

yarn deploy
✏️ Edit your frontend App.jsx in packages/react-app/src to change the targetNetwork to wherever you deployed your contract:

nft9

You should see the correct network in the frontend:

nft10

An instant wallet running on xDAI insired by xdai.io. 🎫 Ready to mint a batch of NFTs for reals?

yarn mint

await tenderlyVerify(
  {contractName: "YourContract",
   contractAddress: yourContract.address
})
Make sure your target network is present in the hardhat networks config, then either update the default network in hardhat.config.js to your network of choice or run:

yarn deploy --network NETWORK_OF_CHOICE
Once verified, they will then be available to view on Tenderly!

nft11

⚔️ Side Quests
🐟 Open Sea
Add your contract to OpenSea ( create -> submit NFTs -> "or add an existing contract" )

(It can take a while before they show up, but here is an example:) https://testnets.opensea.io/assets/0xc2839329166d3d004aaedb94dde4173651babccf/1

🔍 Etherscan Contract Verification
run yarn flatten > flat.txt (You will need to clean up extra junk at the top and bottom of flat.txt. Sorry, rookie stuff here.)

copy the contents of flat.txt to the block explorer and select compiler v0.6.7 and Yes to Optimization (200 runs if anyone asks)

nft12

🔶 Infura
You will need to get a key from infura.io and paste it into constants.js in packages/react-app/src:

nft13

🛳 Ship the app!
⚙️ build and upload your frontend and share the url with your friends...

# build it:

yarn build

# upload it:

yarn surge

yarn s3

yarn ipfs
nft14

👩‍❤️‍👨 Share your public url with a friend and ask them for their address to send them a collectible :)

nft15

Documentation
For a more in-depth explanation, documentation, quick start guide, tutorials, tips and many more resources, visit our documentation site: docs.scaffoldeth.io

💬 Support Chat
Join the telegram support chat 💬 to ask questions and find others building with 🏗 scaffold-eth!
