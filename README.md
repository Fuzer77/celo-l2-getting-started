# 🚀 Celo L2 - Getting Started

Ce projet est un **tutoriel simple** pour débuter avec Celo L2.  
Il montre comment configurer un wallet, obtenir des tokens de test et déployer un petit smart contract sur le testnet **Alfajores**.

---

## 🔧 Étapes rapides

### 1. Installer Metamask
- Télécharge [Metamask](https://metamask.io/).
- Crée un wallet si ce n’est pas déjà fait.

### 2. Ajouter le réseau Alfajores (testnet Celo)
Dans Metamask, ajoute un nouveau réseau :
- **Network Name** : Celo Alfajores Testnet  
- **RPC URL** : https://alfajores-forno.celo-testnet.org  
- **Chain ID** : 44787  
- **Currency Symbol** : CELO  
- **Block Explorer** : https://alfajores.celoscan.io  

### 3. Obtenir des CELO de test
Va sur le faucet officiel : [https://celo.org/developers/faucet](https://celo.org/developers/faucet)  
Colle ton adresse Metamask et récupère des CELO de test.

### 4. Déployer un contrat HelloWorld
Ce contrat Solidity est très simple :

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract HelloWorld {
    string public message;

    constructor(string memory _message) {
        message = _message;
    }

    function setMessage(string memory _newMessage) public {
        message = _newMessage;
    }
}
