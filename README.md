# 🔗 Blockchain Version Control (BVC)

A decentralized version control system inspired by Git, but powered by **blockchain** and **IPFS**.

[![npm version](https://badge.fury.io/js/bvc.svg)](https://badge.fury.io/js/bvc)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## ✨ Features

- 🚀 **Decentralized**: No central server required
- ⛓️ **Blockchain-powered**: Immutable commit history on Ethereum
- 🌐 **IPFS storage**: Decentralized file storage
- 🔐 **Cryptographically secure**: SHA256 file hashing
- 💻 **Git-like CLI**: Familiar commands and workflows

## 📦 Installation

### Global Installation (Recommended)
```bash
npm install -g bvc-eth
```

### Local Installation
```bash
npm install bvc-eth
```

### Manual Installation
```bash
git clone https://github.com/Lviffy/BVC.git
cd BVC
npm install
npm link  # or use: node bin/bvc.js
```

## 🚀 Quick Start

### 1. Configure BVC
```bash
bvc-eth config --setup
```

### 2. Create a Repository
```bash
bvc-eth init my-project
cd my-project
```

### 3. Add Files and Commit
```bash
echo "console.log('Hello BVC!');" > index.js
bvc-eth add index.js
bvc-eth commit -m "Initial commit"
```

### 4. View History
```bash
bvc-eth log
```

## 📋 Commands

| Command | Description | Status |
|---------|-------------|---------|
| `bvc-eth init [name]` | Create new repository | ✅ Working |
| `bvc-eth config` | Configure wallet/blockchain | ✅ Working |
| `bvc-eth add <files>` | Stage files for commit | ✅ Working |
| `bvc-eth commit -m "msg"` | Create commit with IPFS upload | ✅ Working |
| `bvc-eth status` | Show repository status | ✅ Working |
| `bvc-eth log` | View commit history | ✅ Working |
| `bvc-eth push` | Push to blockchain | 🚧 Planned |
| `bvc-eth pull` | Pull from blockchain | 🚧 Planned |
| `bvc-eth clone <id>` | Clone repository | 🚧 Planned |

## ⚙️ Configuration

BVC requires configuration for blockchain and IPFS integration:

```bash
bvc config --setup
```

Required settings:
- **Private Key**: Your wallet private key
- **RPC URL**: Blockchain RPC endpoint (Sepolia, Mainnet, etc.)
- **IPFS Endpoint**: IPFS node URL

## 🏗️ Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   BVC CLI       │───▶│  Smart Contract  │───▶│   Blockchain    │
│   (Commander)   │    │   (Solidity)     │    │   (Ethereum)    │
└─────────────────┘    └──────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│  Local Storage  │    │  File Hashing    │    │      IPFS       │
│   (.bvc/)       │    │   (SHA256)       │    │  (Distributed)  │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

## 🧪 Testing

```bash
npm test
```

## 📜 License

MIT © [Lviffy](https://github.com/Lviffy)

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📞 Support

- 📧 Issues: [GitHub Issues](https://github.com/Lviffy/BVC/issues)
- 📖 Documentation: [Command Guide](./BVC_COMMAND_GUIDE.md)
- 🌐 Website: [GitHub Repository](https://github.com/Lviffy/BVC)

---

**⚠️ Note**: This is an early-stage project. Use at your own risk and test thoroughly before production use.
