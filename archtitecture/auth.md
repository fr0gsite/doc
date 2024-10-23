---
order: 95
label: Authentication
icon: key
tags: [architecture, login]
---

# Authentication

Authentication in this particular blockchain network is achieved through a sophisticated system of key pairs and permissions, offering a balance of security and flexibility. Here's an overview of the process:

* **Public and Private Keys:** The foundation of authentication in this blockchain system is cryptographic key pairs, consisting of a public key and a private key. These keys are used to sign and verify transactions, ensuring that only the holder of the private key can execute transactions on behalf of the associated account.

* **Account Creation:** To interact with the network, one must first create an account. During account creation, specific permissions are assigned to one or more public keys. These keys are then used for authentication and to sign transactions.

* **Permission Levels:** The system employs a multi-level permission structure. Each account can have various levels of permissions for different types of transactions. This flexible structure allows users to set up permissions according to their specific needs, enhancing security and operational efficiency.

* **Signing Transactions:** To perform a transaction, the user signs it with their private key. This signature is used to verify that the transaction has been authorized by the owner of the account. The network checks the signature against the public key associated with the account's permissions.