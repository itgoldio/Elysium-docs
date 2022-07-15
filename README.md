# Elysium-docs

## Install dependencies

1. Install Node.js >= 14.x installed

2. Install npx
```
npm install -g npx
```

## Create solidity project

1. Create project directory

```
mkdir Elysium-commandName
cd Elysium-commandName
```

3. Install locklift
```npm install locklift```

4. Initialize sample solidity project

```npx locklift init --path amazing-locklift-project```

## Build solidity project

```npx locklift build```

more info [github](https://github.com/broxus/ever-locklift)


## Deploy solidity project

### Devnet

#### How to get testnet coins

1. Install [ever wallet](https://l1.broxus.com/)

2. Create a new wallet

[!] important: **Save seed phrase**

3. Change network to testnet in wallet

4. Send wallet address to mentors, mentors will send test tokens.

wallet address like this ```0:022ac4648f0c99014832e678047a7c4eed6ae4e8c806de3a8a1b90177791cc111```

5. Reveive tokens and push "Deploy" button in wallet.

Congratulations to you! You have a wallet and ready to use.

#### How to deploy smart contract

Change ```locklift.config.ts``` 

1. Add section to **LockliftConfig.networks**

```json
    test: {
      // Specify connection settings for https://github.com/broxus/everscale-standalone-client/
      connection: "testnet",
      // This giver is default Wallet
      giver: {
        // Check if you need provide custom giver
        giverFactory: (ever, keyPair, address) => new GiverWallet(ever, keyPair, address),
        address: "0:77ac4648f0c99014832e678047a7c4eed6ae4e8c806de3a8a1b90177a91cc111",
        key: "SEED PHRASE",
      },
      keys: {
        // Use everdev to generate your phrase
        // !!! Never commit it in your repos !!!
        // phrase: "action inject penalty envelope rabbit element slim tornado dinner pizza off blood",
        amount: 20,
      },
      
    },
```

Fill ```address``` your wallet address

Fill ```key``` your private key





