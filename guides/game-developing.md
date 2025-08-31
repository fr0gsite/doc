---
label: Game developing
order: 120
icon: hubot
tags: [guide, games, developing]
---

# Game developing

The frontend is flutter. You can use the game framework [Flame](https://pub.dev/packages/flame).

The backend is a smart contract on the blockchain.
To build and deploy a smart contract you can install [Bolt](https://github.com/VaultaFoundation/Bolt)
which has all the necessary dependencies and allows you to get started quickly.

After the installation of Bolt you need to change the **bolt.config.js** to deploy your contract

```
module.exports = {
    networks:{
        fr0g: {
            node_url: 'https://testnet.fr0g.site:8443',
            chain: 'fr0g',
            accounts: [
                {
                    name: 'your-accountname',
                    // permission: 'owner', // defaults to active
                    private_key: process.env.PRIVATE_KEY
                }
            ]
        }
    },
}
```

and add an file named **deployments/fr0g.ts** where you add your account name
```
odule.exports = async (deployer) => {
    const contract = await deployer.deploy('your-account', 'build/contract', {
        addCode: true
    }).catch(err => {
        console.error(err)
        process.exit(1);
    })
}
```


After making these adjustments, you can use **bolt build && bolt deploy fr0g** to build and deploy your contract.
