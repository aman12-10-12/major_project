# Decentralized Crime Reporting Platform

A blockchain-based anonymous crime reporting system with AI-powered spam detection and decentralized storage.

## 🚨 Just Got Errors? START HERE!

See **`ERROR_FIXES.md`** for solutions to the errors you're seeing.

---

## 📚 Documentation

We have comprehensive guides for every aspect of setup:

| 📄 Guide | 🎯 When to Use |
|----------|---------------|
| **`ERROR_FIXES.md`** | 🚨 **START HERE** if you have errors |
| **`QUICK_START.md`** | Get the app running quickly |
| **`SETUP_GUIDE.md`** | Complete setup instructions |
| **`METAMASK_SETUP.md`** | Install & setup MetaMask wallet |
| **`LIGHTHOUSE_SETUP.md`** | Setup decentralized storage |
| **`TROUBLESHOOTING.md`** | Fix common issues |

---

## ⚡ Quick Start (TL;DR)

### 1. Install Prerequisites
- Node.js & npm
- Python 3.7+
- MetaMask browser extension
- Lighthouse API key (free)

### 2. Backend Setup
```bash
cd decentralized-innovators/backend
python -m venv venv
venv\Scripts\activate          # Windows
# source venv/bin/activate     # Mac/Linux
pip install -r requirements.txt
# Create .env with OPENAI_API_KEY
python app.py
```

### 3. Frontend Setup
```bash
cd decentralized-innovators/frontend
npm install
# Copy env.template to .env and add API keys
npm start
```

### 4. Configure
- Install MetaMask: https://metamask.io/download/
- Get Lighthouse key: https://files.lighthouse.storage/
- Add keys to `.env` files

**Detailed instructions:** See `QUICK_START.md`

---

## 🎯 Features

- ✅ **Anonymous Crime Reporting** with Anon Aadhaar
- ✅ **Blockchain Storage** on Ethereum
- ✅ **AI Spam Detection** via OpenAI
- ✅ **Decentralized File Storage** with Lighthouse/IPFS
- ✅ **Real-time Messaging** with Waku protocol
- ✅ **Gasless Transactions** using Etherspot
- ✅ **Geographic Mapping** with Mapbox
- ✅ **Police Dashboard** for reviewing reports

---

## 🏗️ Tech Stack

### Frontend
- React 18
- Web3.js
- Material-UI
- Mapbox GL
- Waku (decentralized messaging)

### Backend
- Flask (Python)
- OpenAI API
- Flask-CORS

### Blockchain
- Solidity Smart Contracts
- Ethereum/Polygon
- EIP-712 Meta Transactions
- Lighthouse (IPFS/Filecoin)

---

## 📁 Project Structure

```
decentralized-innovators/
├── frontend/              # React application
│   ├── src/
│   │   ├── views/        # React pages/components
│   │   ├── abis/         # Smart contract ABIs
│   │   └── App.js        # Main app component
│   └── env.template      # Environment variables template
├── backend/              # Flask API server
│   ├── app.py           # Main Flask application
│   └── requirements.txt  # Python dependencies
├── contracts/            # Solidity smart contracts
│   ├── TipOff.sol       # Crime reporting contract
│   └── TipToken.sol     # Reward token contract
└── [Documentation files]
```

---

## 🔑 Required API Keys

### 1. Lighthouse Storage (Required for file uploads)
- Get from: https://files.lighthouse.storage/
- Free tier: 1GB storage
- Add to: `frontend/.env`

### 2. OpenAI API (Required for spam detection)
- Get from: https://platform.openai.com/api-keys
- Usage-based pricing
- Add to: `backend/.env`

### 3. MetaMask Wallet (Required for blockchain)
- Install from: https://metamask.io/download/
- Free to use
- Connect to app

**Detailed setup:** See respective setup guides

---

## 🚀 Running the Application

### Development Mode

**Terminal 1 - Backend:**
```bash
cd decentralized-innovators/backend
venv\Scripts\activate    # Windows
python app.py            # Runs on http://localhost:5000
```

**Terminal 2 - Frontend:**
```bash
cd decentralized-innovators/frontend
npm start                # Runs on http://localhost:3000
```

### Access Points
- **Frontend:** http://localhost:3000
- **Backend API:** http://localhost:5000

---

## ⚙️ Configuration

### Frontend Environment (.env)
```env
REACT_APP_APP_ID=
REACT_APP_LIGHTHOUSE_API_KEY=your_lighthouse_key
```

### Backend Environment (.env)
```env
OPENAI_API_KEY=sk-your-openai-key
```

**Note:** Never commit `.env` files to version control!

---

## 🦊 MetaMask Setup

### For Testing:
1. Install MetaMask extension
2. Create test wallet
3. Switch to Sepolia testnet
4. Get test ETH from faucet
5. Connect to localhost:3000

**Full guide:** See `METAMASK_SETUP.md`

---

## 📦 Smart Contract Deployment

### Local Deployment (Ganache)
```bash
# Install Ganache
npm install -g ganache-cli

# Run local blockchain
ganache-cli

# Deploy contracts
truffle migrate --network development
```

### Testnet Deployment
```bash
# Configure truffle-config.js with your network
truffle migrate --network sepolia
```

---

## 🧪 Testing

### Frontend
```bash
cd frontend
npm test
```

### Backend
```bash
cd backend
python -m pytest  # If tests exist
```

---

## 🐛 Common Issues

### "Non-Ethereum browser detected"
→ Install MetaMask: `METAMASK_SETUP.md`

### "500 Internal Server Error" (Lighthouse)
→ Add API key: `LIGHTHOUSE_SETUP.md`

### "Contract address undefined"
→ Deploy contracts or switch network

### React 18 warnings
→ Already fixed in code

**More solutions:** See `ERROR_FIXES.md` and `TROUBLESHOOTING.md`

---

## 📖 How to Use

### For Citizens:
1. Visit the app
2. Connect MetaMask wallet
3. Verify with Anon Aadhaar (anonymous)
4. Submit crime report
5. Stake tokens for credibility
6. Track report status

### For Police:
1. Login to police portal
2. View submitted reports
3. Verify reports on blockchain
4. Take action
5. Update case status

---

## 🔒 Privacy & Security

- **Anonymous Reporting:** Anon Aadhaar for identity verification
- **End-to-End Encryption:** Waku protocol
- **Decentralized Storage:** No single point of failure
- **Blockchain Immutability:** Tamper-proof records
- **Zero-Knowledge Proofs:** Privacy-preserving verification

---

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create feature branch
3. Commit your changes
4. Push to the branch
5. Create Pull Request

---

## 📝 License

[Add your license here]

---

## 🆘 Support

Having issues?

1. ✅ Check `ERROR_FIXES.md`
2. ✅ Read relevant setup guide
3. ✅ Check `TROUBLESHOOTING.md`
4. ✅ Review browser console (F12)
5. ✅ Check terminal output

Still stuck? Open an issue on GitHub!

---

## 🎓 Learning Resources

- **Web3.js:** https://web3js.readthedocs.io/
- **Solidity:** https://docs.soliditylang.org/
- **React:** https://react.dev/
- **MetaMask:** https://docs.metamask.io/
- **Lighthouse:** https://docs.lighthouse.storage/

---

## 🏆 Project Features

### Implemented:
- ✅ Anonymous crime reporting
- ✅ Blockchain storage
- ✅ AI spam detection
- ✅ Decentralized file storage
- ✅ Real-time messaging
- ✅ Police dashboard
- ✅ Token staking system

### Roadmap:
- 🔄 Mobile app
- 🔄 Multi-language support
- 🔄 Enhanced analytics
- 🔄 Integration with more chains

---

## 📊 System Requirements

### Minimum:
- Node.js 14+
- Python 3.7+
- 4GB RAM
- Modern web browser

### Recommended:
- Node.js 18+
- Python 3.10+
- 8GB RAM
- Chrome/Brave with MetaMask

---

## 🌟 Acknowledgments

Built with:
- React & Create React App
- Web3.js & Ethereum
- Lighthouse & IPFS
- OpenAI
- Material-UI
- And many other open-source projects

---

## 📞 Quick Help

| Problem | Solution |
|---------|----------|
| Can't run app | `QUICK_START.md` |
| MetaMask errors | `METAMASK_SETUP.md` |
| File upload fails | `LIGHTHOUSE_SETUP.md` |
| Backend errors | Check OpenAI key in `backend/.env` |
| Contract errors | Deploy contracts or switch network |

---

**🚀 Ready to start? → Open `ERROR_FIXES.md` or `QUICK_START.md`**

