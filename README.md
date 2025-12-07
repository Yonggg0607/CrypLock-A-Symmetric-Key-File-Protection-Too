# 🔐 CrypLock – Simple AES-256 File Locker

CrypLock is a small Python tool that lets you **encrypt and decrypt files** using **AES-256** with a simple Tkinter GUI.

---

## ⭐ Features
- AES-256 encryption (strong security)
- CBC mode with random IV
- Generate key button
- Encrypt any file → saves as `.enc`
- Decrypt `.enc` file back to original
- Clean and simple GUI (Tkinter)

---

## 📦 Requirements
Install cryptography:

```
pip install cryptography
```

Tkinter comes with most Python installations.

---

## ▶️ How to Run
```
python CrypLock.py
```

---

## 🔑 How It Works

### 1. Generate Key  
Creates a **256-bit (32-byte)** AES key and saves it as **CrypLock.key**.

### 2. Encrypt File  
- Choose a file  
- App loads the key  
- Pads the data (PKCS7)  
- Encrypts using AES-256-CBC  
- File is saved as:  
  `originalname.ext.enc`

### 3. Decrypt File  
- Choose the `.enc` file  
- App loads the key  
- Reads IV + ciphertext  
- Decrypts + removes padding  
- Restores original file name

---

## ⚠️ Important
- **CrypLock.key must be kept safe.** Losing it means you cannot decrypt your files.
- The key must be in the **same folder** as the program.
- Do not rename `.enc` files.

---

## 📂 Project Files
```
CrypLock.py
CrypLock.key   (generated after first use)
README.md
```
