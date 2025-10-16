# Decentralized Innovators - Setup Guide

A decentralized crime reporting application with React frontend, Flask backend, and Ethereum smart contracts.

## 🔧 Prerequisites

Before running this project, ensure you have:

- **Node.js** (v14 or higher) and npm
- **Python** (v3.7 or higher)
- **MetaMask** browser extension ([Download here](https://metamask.io/download/))
- **OpenAI API Key** ([Get one here](https://platform.openai.com/api-keys))

---

## 🚀 Installation & Setup

### 1️⃣ Backend Setup (Flask API)

```bash
# Navigate to backend directory
cd decentralized-innovators/backend

# Create a virtual environment (recommended)
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate

# On macOS/Linux:
# source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

**Create `.env` file in backend directory:**

```bash
# backend/.env
OPENAI_API_KEY=your_openai_api_key_here
```

**Run the backend server:**

```bash
python app.py
```

✅ Backend will run on **http://localhost:5000**

---

### 2️⃣ Frontend Setup (React App)

Open a **new terminal** (keep backend running):

```bash
# Navigate to frontend directory
cd decentralized-innovators/frontend

# Install dependencies
npm install

# Start the React development server
npm start
```

✅ Frontend will run on **http://localhost:3000**

---

## 🦊 MetaMask Setup

### Important: Configure MetaMask

1. **Install MetaMask** browser extension if not already installed
2. **Create/Import a wallet** in MetaMask
3. **Connect to a test network:**
   - For local development: Use Ganache or Hardhat local network
   - For testnet: Use Sepolia, Goerli, or Mumbai testnet
4. **Get test ETH/MATIC** from faucets (if using testnet)

### Connect to Local Blockchain (Optional)

If you want to deploy contracts locally:

```bash
# Install Ganache globally
npm install -g ganache-cli

# Run local blockchain
ganache-cli
```

---

## 🔗 Smart Contracts Setup

The project includes Solidity smart contracts in the `contracts/` directory:

- `TipOff.sol` - Main contract for crime reporting
- `TipToken.sol` - Token contract for rewards
- `EIP712MetaTransaction.sol` - For gasless transactions

### Deploy Contracts (if needed)

You'll need Truffle or Hardhat to deploy:

```bash
# Install Truffle (if not installed)
npm install -g truffle

# In the project root
truffle compile
truffle migrate --network development
```

---

## ⚠️ Common Issues & Solutions

### Issue 1: "Contract address undefined"

**Cause:** Smart contracts not deployed to the current network

**Solution:**
- Make sure you're connected to the correct network in MetaMask
- Deploy contracts to your current network
- Or switch MetaMask to a network where contracts are deployed

### Issue 2: "Non-Ethereum browser detected"

**Cause:** MetaMask not installed or not enabled

**Solution:**
- Install MetaMask browser extension
- Refresh the page after installation
- Click "Connect" when MetaMask prompts you

### Issue 3: "User denied account access"

**Cause:** You rejected the MetaMask connection request

**Solution:**
- Refresh the page
- Click "Connect" when MetaMask prompts
- Or manually connect via MetaMask extension

### Issue 4: Backend errors about OpenAI API

**Cause:** Missing or invalid OpenAI API key

**Solution:**
- Create a `.env` file in the `backend/` directory
- Add your OpenAI API key: `OPENAI_API_KEY=sk-...`
- Restart the backend server

### Issue 5: npm vulnerabilities warning

**Cause:** Outdated packages (common in projects)

**Solution:**
```bash
# Review vulnerabilities
npm audit

# Fix non-breaking issues
npm audit fix

# For more aggressive fixes (may break things)
npm audit fix --force
```

---

## 📝 Environment Variables

### Backend `.env` file:
```env
OPENAI_API_KEY=your_openai_api_key_here
```

### Frontend `.env` file (create if needed):
```env
REACT_APP_APP_ID=your_app_id_here
```

---

## 🎯 Features

- **Anonymous Crime Reporting** using Anon Aadhaar
- **AI-Powered Spam Detection** via OpenAI
- **Blockchain-Based Storage** with Ethereum
- **Real-time Messaging** with Waku protocol
- **Gasless Transactions** using Etherspot
- **Geographic Mapping** with Mapbox
- **Police Dashboard** for reviewing reports

---

## 🔍 Project Structure

```
decentralized-innovators/
├── backend/              # Flask API server
│   ├── app.py           # Main Flask application
│   └── requirements.txt # Python dependencies
├── frontend/            # React application
│   ├── src/
│   │   ├── views/      # React pages/components
│   │   ├── abis/       # Smart contract ABIs
│   │   └── App.js      # Main React component
│   └── package.json    # Node dependencies
└── contracts/          # Solidity smart contracts
```

---

## 🛠️ Development Tips

1. **Keep both servers running** (backend and frontend)
2. **Check MetaMask network** - must match deployed contracts
3. **Monitor console** for Web3 connection issues
4. **Clear browser cache** if experiencing strange behavior
5. **Use React DevTools** for debugging React components

---

## 📚 Additional Resources

- [Web3.js Documentation](https://web3js.readthedocs.io/)
- [React Documentation](https://react.dev/)
- [MetaMask Documentation](https://docs.metamask.io/)
- [Flask Documentation](https://flask.palletsprojects.com/)
- [Solidity Documentation](https://docs.soliditylang.org/)

---

## 🐛 Getting Help

If you encounter issues:

1. Check the browser console for errors
2. Verify MetaMask is connected to the right network
3. Ensure backend server is running on port 5000
4. Check that all environment variables are set
5. Make sure you have test ETH/MATIC in your wallet

---

## ✅ Verification Checklist

Before using the app, verify:

- [ ] MetaMask installed and wallet created
- [ ] Backend running on http://localhost:5000
- [ ] Frontend running on http://localhost:3000
- [ ] OpenAI API key configured in backend/.env
- [ ] MetaMask connected to correct network
- [ ] Smart contracts deployed (if using blockchain features)

---

## 📞 Support

For more help, check:
- Browser console logs
- Backend terminal output
- MetaMask notifications
- Network requests in DevTools

Happy coding! 🚀

