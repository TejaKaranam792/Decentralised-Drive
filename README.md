<h1 align="center">🚀 Decentralised Drive</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Web3-Decentralized-blueviolet?style=for-the-badge&logo=ethereum"/>
  <img src="https://img.shields.io/badge/React-Frontend-61DBFB?style=for-the-badge&logo=react"/>
  <img src="https://img.shields.io/badge/Hardhat-Smart%20Contracts-f1c232?style=for-the-badge&logo=ethereum"/>
  <img src="https://img.shields.io/badge/Ethers.js-Blockchain-yellow?style=for-the-badge&logo=javascript"/>
</p>

---

## 🌐 Overview

**Decentralised Drive** is a **Web3-based file storage DApp** that allows users to **upload, access, and manage files securely on the blockchain** using IPFS integration and smart contracts for ownership verification.

Forget central servers — your data, your control.  
🔐 100% Decentralized. 💡 Transparent. 💎 Immutable.

---

## ✨ Features

- 📤 **Upload Files** directly to decentralized storage  
- 👤 **Wallet Authentication** with MetaMask  
- 🔒 **Smart Contract Verification** for ownership  
- 🌍 **Accessible from anywhere** (no centralized backend)  
- ⚙️ **Seamless integration** between React + Hardhat + Ethers  
- 🎨 **Modern UI** built with React

---

## 🏗️ Tech Stack

| Layer | Technologies Used |
|-------|-------------------|
| **Frontend** | React, JavaScript, CSS |
| **Blockchain** | Solidity, Hardhat |
| **Web3 Interaction** | Ethers.js |
| **Storage** | IPFS / Pinata |
| **Network** | Ethereum / Sepolia Testnet |

---

## ⚡ Quick Start

### 1️⃣ Clone the repository
```bash
git clone https://github.com/TejaKaranam792/Decentralised-Drive.git
cd Decentralised-Drive\client
2️⃣ Install dependencies
bash
Copy code
npm install
3️⃣ Run the local blockchain (in another terminal)
bash
Copy code
npx hardhat node
4️⃣ Deploy contracts
bash
Copy code
npx hardhat run scripts/deploy.js --network localhost
5️⃣ Start the frontend
bash
Copy code
npm start
6️⃣ Connect your MetaMask wallet
Switch to Localhost 8545 or Sepolia testnet, then you’re live!

🧠 Smart Contract Snippet
solidity
Copy code
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.26;

contract Upload {
    mapping(address => string[]) public userFiles;

    function addFile(string memory fileUrl) public {
        userFiles[msg.sender].push(fileUrl);
    }

    function getFiles(address user) public view returns (string[] memory) {
        return userFiles[user];
    }
}
💡 Every file’s metadata is stored immutably on-chain, linked with the uploader’s wallet address.

📸 Screenshots
Upload Page	Connected Wallet	File List

🧩 Folder Structure
bash
Copy code
Decentralised-Drive/
│
├── client/              # React Frontend
│   ├── src/
│   │   ├── App.js
│   │   ├── components/
│   │   └── styles/
│   └── package.json
│
├── contracts/           # Solidity Smart Contracts
│   └── Upload.sol
│
├── scripts/             # Hardhat Deployment Scripts
├── hardhat.config.js    # Network & Compiler Config
└── README.md
🚀 Future Enhancements
💾 Encrypted file uploads with private key access

🌐 Multi-chain support (Polygon, Arbitrum)

👥 User dashboard for file analytics

🪙 NFT-based file ownership

🧑‍💻 Author
👋 Teja Karanam
💼 Blockchain Developer | React & Web3 Enthusiast
📧 tejakaranam76252@gmail.com
