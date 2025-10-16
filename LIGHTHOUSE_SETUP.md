# Lighthouse Storage Setup Guide

Lighthouse is a decentralized storage solution (similar to IPFS/Filecoin) used by this application to store crime report data and attachments.

## 🚨 Why You're Getting Errors

The error you're seeing:
```
POST https://node.lighthouse.storage/api/v0/add?wrap-with-directory=false 500 (Internal Server Error)
```

This happens because:
1. **Missing API Key** - You need a Lighthouse API key
2. **Invalid API Key** - Your key might be incorrect or expired

---

## 🔑 How to Get Lighthouse API Key

### Step 1: Visit Lighthouse Files
Go to: **https://files.lighthouse.storage/**

### Step 2: Sign Up / Login
- Click "Sign in with GitHub"
- Authorize the application
- Complete the registration

### Step 3: Get API Key
1. Once logged in, look for the **"API Keys"** section in the dashboard
2. Click **"Create New API Key"** or **"Generate API Key"**
3. Give it a name (e.g., "Crime Reporting App")
4. **Copy the generated API key** (it will look like a long string)

### Step 4: Add to Your Project
1. In your project, go to: `decentralized-innovators/frontend/`
2. Copy the `env.template` file and rename it to `.env`
3. Open the `.env` file
4. Find this line:
   ```
   REACT_APP_LIGHTHOUSE_API_KEY=
   ```
5. Paste your API key after the `=` sign:
   ```
   REACT_APP_LIGHTHOUSE_API_KEY=7b1e4e4f.a8c9d8e7f6g5h4i3j2k1l0m9n8o7p6q5
   ```
6. **Save the file**

### Step 5: Restart the App
```bash
# Stop the running server (Ctrl+C in terminal)
# Then restart:
npm start
```

---

## 📝 Complete .env File Example

Your `frontend/.env` file should look like this:

```env
# Anon Aadhaar App ID (optional)
REACT_APP_APP_ID=

# Lighthouse Storage API Key (REQUIRED)
REACT_APP_LIGHTHOUSE_API_KEY=7b1e4e4f.a8c9d8e7f6g5h4i3j2k1l0m9n8o7p6q5
```

---

## ✅ Verify It's Working

After setting up:

1. **Restart the development server**
2. **Open the browser console** (F12)
3. **Try uploading a file** in the app
4. You should see:
   - No more 500 errors
   - Success message: "File uploaded successfully!"
   - Console log with IPFS hash

---

## 🔍 Troubleshooting

### Issue: Still getting 500 errors

**Check:**
1. API key is copied correctly (no extra spaces)
2. File is named exactly `.env` (not `.env.txt`)
3. File is in `frontend/` directory
4. Server was restarted after adding key

### Issue: API key not found error

**Solution:**
```bash
# Make sure .env file exists
cd decentralized-innovators/frontend
ls -la .env  # On Windows: dir .env

# If not found, copy from template:
cp env.template .env  # On Windows: copy env.template .env

# Then add your API key and restart
```

### Issue: Invalid API key

**Solution:**
1. Go back to https://files.lighthouse.storage/
2. Regenerate your API key
3. Update `.env` file with new key
4. Restart server

---

## 🎯 What Lighthouse Does in This App

1. **Stores crime reports** - Text data as JSON
2. **Stores evidence files** - Images, videos, documents
3. **Returns IPFS hashes** - Used as references on blockchain
4. **Provides decentralized access** - Anyone can verify via IPFS

---

## 🔗 Useful Links

- **Lighthouse Dashboard**: https://files.lighthouse.storage/
- **Lighthouse Docs**: https://docs.lighthouse.storage/
- **API Documentation**: https://docs.lighthouse.storage/lighthouse-1/how-to/upload
- **IPFS Gateway**: https://gateway.lighthouse.storage/ipfs/

---

## 💡 Alternative: Run Without Lighthouse (For Testing)

If you just want to test the app without file uploads:

1. Don't add any API key
2. Skip the file upload step when submitting reports
3. Only text-based features will work

**Note:** Some features will be limited without Lighthouse storage.

---

## 🚀 Free Tier Limits

Lighthouse free tier includes:
- **1 GB of storage**
- Unlimited uploads
- Permanent storage

Perfect for development and testing!

