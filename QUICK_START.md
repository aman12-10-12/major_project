# Quick Start Guide

## ⚡ Get Running in 5 Minutes

### 🚨 Got Errors? See `ERROR_FIXES.md` first!

---

## Step-by-Step Setup

### Step 1: Backend Setup
```bash
cd decentralized-innovators/backend
python -m venv venv
venv\Scripts\activate    # Windows
pip install -r requirements.txt

# Create .env file with:
# OPENAI_API_KEY=your_key_here

python app.py
```

### Step 2: Frontend Setup (New Terminal)
```bash
cd decentralized-innovators/frontend
npm install
npm start
```

### Step 3: MetaMask
1. Install [MetaMask extension](https://metamask.io/download/)
2. Create a wallet
3. Connect when prompted

---

## 🎯 Access the App

- **Frontend:** http://localhost:3000
- **Backend:** http://localhost:5000

---

## ⚠️ Quick Fixes

**"Contract address undefined"?**
- Install & connect MetaMask
- Refresh the page after connecting

**Backend errors?**
- Add OpenAI API key to `backend/.env`

**Still stuck?**
- See detailed guide in `SETUP_GUIDE.md`

