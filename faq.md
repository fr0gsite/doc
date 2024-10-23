---
label: FAQ
icon: question
order: 998
---


## How can i get an account ?

* An existing user invites you
* Free account issued by the Foundation. [Found here](https://create.fr0g.site/)

## Where is the private key stored?

The [Flutter Application](https://github.com/fr0gsite/FlutterFr0g) use the [flutter_secure_storage](https://pub.dev/packages/flutter_secure_storage) library which provides an secure storage for each platform (Android, IOS, Web, ...). All important information like privatekey or username are stored there.

**Please note for web** that the library use an experimental implementation of WebCrypto. **This means that the use is at your own risk at this time.** Feedback to improve it is welcome.


## Where and how can I invest in the project ?
  
* The project is currently not traded on any stock exchange, but the core team is working on it. As soon as there is news about this, it will be announced on official channels.
* As a core developer or core team member, you will receive system tokens as payment/reward. If you are interested to work with us, please [contact us](https://doc.fr0g.site/participate/overview/)
* You can become an Block Producer and earn tokens. [more infos](https://doc.fr0g.site/participate/blockproducers/)
  
## Where are pictures and videos stored ?

The content is stored on the IPFS network [(This 5 min video explaining best IPFS)](https://www.youtube.com/watch?v=TbagkanDeiU). The files are stored on the computers of the users or are stored by service providers for users.

## Where is the code hosted ?
The code is hosted on [GitHub](https://github.com/fr0gsite).

## Where can I report errors or problems?

### For the App
* [Github](https://github.com/fr0gsite/FlutterFr0g/issues)
### For the Chain
* [Github](https://github.com/fr0gsite/blockchain/issues)

# What is the difference between active and owner permission

Both are main types of permissions in the EOS blockchain. The **Owner** permission provides the highest level of authority and allows a user to make significant changes to the account, including changing other permissions. This authorization should be kept very secure and should only be used for essential changes. The **Active** authorization, on the other hand, is intended for everyday actions.

In the case that an unauthorized person gets access to the Private key from the **Active** permission, the Owner permission can be used to **reset the Public key** from the **Active** permission and the attacker have no access anymore.

## What are the official channels ?

* [Telegram](https://t.me/fr0gsite)
 
