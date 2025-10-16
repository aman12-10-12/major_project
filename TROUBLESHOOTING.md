# Troubleshooting Guide

This guide addresses common errors you might encounter.

## 🎯 Quick Links to Specific Guides

- **MetaMask Issues?** → See `METAMASK_SETUP.md`
- **Lighthouse Storage Errors?** → See `LIGHTHOUSE_SETUP.md`
- **General Setup?** → See `SETUP_GUIDE.md` or `QUICK_START.md`

---

## ✅ Fixed Issues

### 1. React 18 Warning
**Error:**
```
Warning: ReactDOM.render is no longer supported in React 18
```

**Status:** ✅ **FIXED**
- Updated `src/index.js` to use React 18's `createRoot` API
- The warning will no longer appear

---

### 2. Web3 TypeError
**Error:**
```
TypeError: Cannot read properties of undefined (reading 'eth')
contract address: undefined
account address: undefined
```

**Status:** ✅ **FIXED**
- Added proper error handling in `App.js`
- Web3 initialization now checks if MetaMask is available
- Updated to modern MetaMask API (`eth_requestAccounts`)

**To use the blockchain features:**
1. Install MetaMask browser extension
2. Create or import a wallet
3. Refresh the page
4. Click "Connect" when MetaMask prompts you

---

## ⚠️ Warnings You Can Ignore

### ESLint Warnings
These are code quality warnings (unused variables, missing alt tags, etc.):
```
'ERR_INVALID_RESPONSE' is defined but never used
img elements must have an alt prop
```

**Impact:** None - app works fine
**Fix:** Optional (clean up later if needed)

---

### Source Map Warnings
```
Failed to parse source map from '@chainsafe/is-ip'
```

**Impact:** None - just developer tooling
**Fix:** Ignore or add to `.env`:
```
GENERATE_SOURCEMAP=false
```

---

### Babel Warning
```
"@babel/plugin-proposal-private-property-in-object" package warning
```

**Impact:** None - app compiles successfully
**Fix (optional):**
```bash
npm install --save-dev @babel/plugin-proposal-private-property-in-object
```

---

## 🔍 HTML Nesting Warnings

### Warning: `<a>` cannot appear as descendant of `<a>`
**Location:** IndexNavbar component

**Impact:** Minor - may affect styling
**Fix:** Update the navbar component to not nest anchor tags

### Warning: `<ul>` cannot appear as descendant of `<p>`
**Location:** Index page

**Impact:** Minor - may affect styling
**Fix:** Move `<ul>` outside of `<p>` tags

---

## 🦊 MetaMask Connection Issues

### "Non-Ethereum browser detected"

**Cause:** MetaMask not installed or disabled

**Solution:**
1. Install MetaMask: https://metamask.io/download/
2. Restart your browser
3. Refresh the application
4. You should see a connection prompt

---

### Contract Not Deployed

**Error:**
```
Smart contract not deployed to detected network
```

**Cause:** You're on a network where contracts aren't deployed

**Solutions:**

**Option 1: Use Test Network (Recommended for testing)**
1. Open MetaMask
2. Click network dropdown (top of MetaMask)
3. Enable "Show test networks" in settings
4. Switch to Sepolia or Goerli
5. Get test ETH from a faucet

**Option 2: Deploy Locally**
```bash
# Install Ganache
npm install -g ganache-cli

# Run local blockchain
ganache-cli

# In MetaMask:
# - Add Custom RPC
# - Network Name: Ganache
# - RPC URL: http://127.0.0.1:8545
# - Chain ID: 1337

# Deploy contracts
truffle migrate --network development
```

---

## 🔧 Backend Issues

### OpenAI API Errors

**Error:**
```
No API key provided
```

**Solution:**
1. Get API key from https://platform.openai.com/api-keys
2. Create `backend/.env`:
   ```
   OPENAI_API_KEY=sk-your-key-here
   ```
3. Restart backend server

---

### CORS Errors

**Error:**
```
Access to fetch at 'http://localhost:5000' has been blocked by CORS
```

**Solution:**
- Backend already has CORS enabled
- Check that backend is running on port 5000
- Verify both frontend and backend are running

---

## 📊 Verification Steps

### Check Backend is Running:
```bash
curl http://localhost:5000/detectSpam2 -X POST -H "Content-Type: application/json" -d "{\"chunk\":\"test\"}"
```

### Check Frontend is Running:
Open http://localhost:3000 in browser

### Check MetaMask Connection:
```javascript
// In browser console:
window.ethereum ? "MetaMask installed ✅" : "MetaMask NOT installed ❌"
```

---

## 🚨 Critical Issues

If you see these, the app won't work:

### 1. Backend Not Running
**Symptom:** Network errors in console
**Check:** Is `python app.py` running in terminal?

### 2. Port Already in Use
**Symptom:** "Something is already running on port 3000"
**Fix:** Kill the process or run on different port (app will prompt)

### 3. Module Not Found Errors
**Symptom:** Import errors in terminal
**Fix:**
```bash
# Frontend
cd frontend
npm install

# Backend
cd backend
pip install -r requirements.txt
```

---

## 💡 Pro Tips

1. **Open Browser DevTools** (F12) to see detailed errors
2. **Check Network Tab** to see if API calls are failing
3. **Watch Terminal Output** for backend errors
4. **MetaMask Console Logs** show connection status
5. **Clear Browser Cache** if seeing stale data

---

## 📞 Still Having Issues?

1. ✅ Check all prerequisites are installed
2. ✅ Verify both servers are running
3. ✅ Ensure MetaMask is connected
4. ✅ Check browser console for errors
5. ✅ Review terminal output for errors

Most issues are related to:
- MetaMask not installed/connected
- Backend not running
- Missing environment variables
- Network mismatch (contracts not deployed)

