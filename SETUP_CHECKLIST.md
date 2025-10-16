# Setup Checklist ✅

Use this checklist to track your setup progress. Check off items as you complete them!

---

## 📋 Phase 1: Prerequisites

- [ ] **Node.js installed** (check: `node --version` should show v14+)
- [ ] **npm installed** (check: `npm --version`)
- [ ] **Python installed** (check: `python --version` should show 3.7+)
- [ ] **Git installed** (if cloning repo)

---

## 📋 Phase 2: Basic Installation

### Backend
- [ ] Navigated to `decentralized-innovators/backend`
- [ ] Created virtual environment (`python -m venv venv`)
- [ ] Activated virtual environment
  - Windows: `venv\Scripts\activate`
  - Mac/Linux: `source venv/bin/activate`
- [ ] Installed dependencies (`pip install -r requirements.txt`)
- [ ] Backend installs successfully (no errors)

### Frontend
- [ ] Navigated to `decentralized-innovators/frontend`
- [ ] Ran `npm install`
- [ ] Frontend installs successfully (warnings OK, no fatal errors)

---

## 📋 Phase 3: MetaMask Setup

- [ ] **Visited** https://metamask.io/download/
- [ ] **Installed** MetaMask browser extension
- [ ] **Created** new wallet (or imported existing)
- [ ] **Saved** recovery phrase securely (on paper!)
- [ ] **See** MetaMask fox icon in browser toolbar
- [ ] **Can open** MetaMask and see your address

**Need help?** See `METAMASK_SETUP.md`

---

## 📋 Phase 4: Lighthouse Storage Setup

- [ ] **Visited** https://files.lighthouse.storage/
- [ ] **Signed in** with GitHub
- [ ] **Generated** API key from dashboard
- [ ] **Copied** API key (long string starting with letters/numbers)
- [ ] **Created** `frontend/.env` file from `env.template`
- [ ] **Added** API key to `.env` file:
  ```
  REACT_APP_LIGHTHOUSE_API_KEY=your_key_here
  ```
- [ ] **Saved** the `.env` file

**Need help?** See `LIGHTHOUSE_SETUP.md`

---

## 📋 Phase 5: OpenAI Setup (Optional)

Only needed for AI spam detection features.

- [ ] **Visited** https://platform.openai.com/api-keys
- [ ] **Created** account / logged in
- [ ] **Generated** API key
- [ ] **Created** `backend/.env` file
- [ ] **Added** API key to `backend/.env`:
  ```
  OPENAI_API_KEY=sk-your_key_here
  ```
- [ ] **Saved** the file

**Skip if:** You don't want AI features (app will still work)

---

## 📋 Phase 6: Running the Application

### Start Backend
- [ ] **Opened** terminal/command prompt
- [ ] **Navigated** to `decentralized-innovators/backend`
- [ ] **Activated** virtual environment
- [ ] **Ran** `python app.py`
- [ ] **See** message: "Running on http://127.0.0.1:5000"
- [ ] **Keep** this terminal open

### Start Frontend
- [ ] **Opened** NEW terminal/command prompt
- [ ] **Navigated** to `decentralized-innovators/frontend`
- [ ] **Ran** `npm start`
- [ ] **Browser** opens automatically to http://localhost:3000
- [ ] **Can see** the app interface
- [ ] **Keep** this terminal open too

---

## 📋 Phase 7: Connect MetaMask

- [ ] **App loaded** in browser at localhost:3000
- [ ] **MetaMask popup** appeared automatically (or click Connect button)
- [ ] **Selected** account to connect
- [ ] **Clicked** "Next" → "Connect"
- [ ] **See** your address connected in the app
- [ ] **Open** browser console (F12) - no "Web3 not initialized" errors

**If no popup:** Click the Connect Wallet button in the app

---

## 📋 Phase 8: Network Configuration

Choose ONE option:

### Option A: Use Testnet (Recommended)
- [ ] **Opened** MetaMask
- [ ] **Clicked** network dropdown (top of MetaMask)
- [ ] **Enabled** "Show test networks" in settings
- [ ] **Selected** Sepolia or Goerli testnet
- [ ] **Got** test ETH from faucet:
  - Sepolia: https://sepoliafaucet.com/
  - Goerli: https://goerlifaucet.com/
- [ ] **See** test ETH balance in MetaMask

### Option B: Use Local Blockchain
- [ ] **Installed** Ganache (`npm install -g ganache-cli`)
- [ ] **Ran** `ganache-cli` in terminal
- [ ] **Added** local network to MetaMask:
  - Network Name: Localhost 8545
  - RPC URL: http://127.0.0.1:8545
  - Chain ID: 1337
- [ ] **Switched** to Localhost network in MetaMask

---

## 📋 Phase 9: Deploy Smart Contracts

Choose based on your network:

### For Local (Ganache)
- [ ] **Installed** Truffle (`npm install -g truffle`)
- [ ] **Ran** `truffle migrate --network development`
- [ ] **See** contract addresses in output
- [ ] **No errors** during deployment

### For Testnet
- [ ] **Configured** truffle-config.js with testnet settings
- [ ] **Added** private key to config
- [ ] **Ran** `truffle migrate --network sepolia` (or your testnet)
- [ ] **See** contract addresses in output

**Skip if:** Using pre-deployed contracts

---

## 📋 Phase 10: Verification

### Frontend Check
- [ ] ✅ App loads at http://localhost:3000
- [ ] ✅ No React errors in console
- [ ] ✅ Can navigate through pages
- [ ] ✅ UI looks correct

### Backend Check
- [ ] ✅ Backend running at http://localhost:5000
- [ ] ✅ No errors in backend terminal
- [ ] ✅ Can see Flask startup message

### MetaMask Check
- [ ] ✅ MetaMask connected
- [ ] ✅ Address visible in app
- [ ] ✅ On correct network
- [ ] ✅ Have some ETH (test or local)

### Browser Console Check (F12)
- [ ] ✅ "Web3 initialized successfully" message
- [ ] ✅ Account address shown
- [ ] ✅ Network ID shown
- [ ] ❌ No "Web3 not initialized" errors
- [ ] ❌ No "Non-Ethereum browser" errors

### Lighthouse Check
- [ ] ✅ No 500 errors when uploading files
- [ ] ✅ "File uploaded successfully" toast message
- [ ] ❌ No "API key missing" errors

---

## 📋 Phase 11: Test Features

### Basic Features
- [ ] **Can** browse the homepage
- [ ] **Can** view mental health resources
- [ ] **Can** navigate to different pages

### Blockchain Features
- [ ] **Can** open crime reporting form
- [ ] **Can** fill out form fields
- [ ] **Can** select location on map
- [ ] **Can** submit report (MetaMask confirmation appears)
- [ ] **Transaction** succeeds in MetaMask

### File Upload
- [ ] **Can** attach files to report
- [ ] **Files** upload successfully (no 500 errors)
- [ ] **See** IPFS hash in console

### AI Features (if OpenAI configured)
- [ ] **Spam detection** works
- [ ] **Backend** processes requests
- [ ] **No** OpenAI errors

---

## 🎉 Success Criteria

You've successfully set up the app if:

✅ Both frontend and backend are running without errors
✅ MetaMask is connected and showing your address
✅ Can browse all pages without crashes
✅ Can submit a test crime report
✅ Files upload successfully (if Lighthouse configured)
✅ No critical errors in console

---

## ❌ Troubleshooting

If ANY checkbox above is not checked:

| Issue | See This File |
|-------|--------------|
| Can't install dependencies | `SETUP_GUIDE.md` |
| MetaMask problems | `METAMASK_SETUP.md` |
| Lighthouse errors | `LIGHTHOUSE_SETUP.md` |
| Specific errors | `ERROR_FIXES.md` |
| General issues | `TROUBLESHOOTING.md` |

---

## 📊 Progress Tracker

Count your checkmarks:

- **0-10 checked:** Just starting - follow `QUICK_START.md`
- **11-25 checked:** Making progress - keep going!
- **26-40 checked:** Almost there - check what's missing
- **40+ checked:** Almost done - final verification!
- **All checked:** 🎉 Congratulations! You're all set!

---

## 🔄 Quick Reset

If you need to start over:

```bash
# Backend
cd backend
deactivate           # Exit venv
rm -rf venv         # Remove venv
rm .env             # Remove config

# Frontend  
cd frontend
rm -rf node_modules # Remove packages
rm .env             # Remove config

# Then start from Phase 2
```

---

## 💡 Tips

- ✅ Do phases in order
- ✅ Don't skip prerequisites
- ✅ Keep terminals open while app runs
- ✅ Check off items as you go
- ✅ Take breaks between phases
- ✅ Ask for help if stuck (see docs)

---

## 🎯 Minimal Working Setup

Want just the basics working?

**Required:**
- [x] Phase 1: Prerequisites
- [x] Phase 2: Basic Installation
- [x] Phase 6: Running the Application

**Recommended:**
- [x] Phase 3: MetaMask Setup
- [x] Phase 4: Lighthouse Storage

**Optional:**
- [ ] Phase 5: OpenAI (can skip)
- [ ] Phase 9: Deploy Contracts (if not pre-deployed)

Start with Required, add Recommended for full features!

---

**Ready to begin? Start with Phase 1! 🚀**

