# Neon's Color Changing Noun

![Color chaning noun .gif](https://media.giphy.com/media/7SrmPnpz1mI2bvdmRy/giphy.gif)

This is a derivative [Noun](https://nouns.wtf/) NFT that changes color every time it is viewed.

[View on OpenSea](https://opensea.io/collection/neons-color-changing-noun)

Here are the four colors this Noun can be:

<img src="https://arweave.net/_GXKwDn7-PxJj0uEHQDkd9Gpy3MH0JnmN8fq6hgghJ4" width="125" height="125" />
<img src="https://arweave.net/-DFiPFisMdOAwrd-fAoLldUieyTrw_NdCkcrc6VEur0" width="125" height="125" />
<img src="https://arweave.net/zH26a2lCOUL53hvU0m8HNQC7ReK5pLSnc5SxqndQc_4" width="125" height="125" />
<img src="https://arweave.net/yqic309BA9c7lYyOVoY1CrluSAB0TEbZGb4d2pZF0uQ" width="125" height="125" />

Four pairs of images and metadata are stored on Arweave and a manifest file is utilized to make each one have the same base URI. Here are the Arweave URLs:
```
https://arweave.net/gU0SB5pNS5DfrfZtrP3kZSW1AyYMWdzG6JtUSYsADGM/1 // 💠 Cyan
https://arweave.net/gU0SB5pNS5DfrfZtrP3kZSW1AyYMWdzG6JtUSYsADGM/2 // 💞 Fuchsia
https://arweave.net/gU0SB5pNS5DfrfZtrP3kZSW1AyYMWdzG6JtUSYsADGM/3 // 🦋 Amber
https://arweave.net/gU0SB5pNS5DfrfZtrP3kZSW1AyYMWdzG6JtUSYsADGM/4 // 🌱 Emerald
```

When the contract's `tokenURI` is queried, it uses the `block.timestamp % 4 + 1` to create a pseudo-random number between 1 and 4 then tacks that number onto the Arweave base URI and returns it. That way, just about each time `tokenURI` gets queried, it returns a different set of image and metadata.

The contract utilizes iainnash's [gwei-slim-erc721](https://github.com/iainnash/gwei-slim-erc721) to reduce gas costs.

This code is open-source. Please clone, fork, and code to your heart's content!

---

Deploy:
```
npx hardhat deploy --network <rinkeby or mainnet> --tags NeonsColorChangingNoun
```
The command to verify on Etherscan will be printed following a successful deployment.
