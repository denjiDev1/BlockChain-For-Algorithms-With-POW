
# 🛠️ Blockchain Data Proof System with IPFS

A minimal proof-of-work blockchain project that integrates **IPFS** for decentralized data storage. This system allows you to upload any file, generate its hash via IPFS, and then record that hash on a blockchain as a verified proof. Later, users can retrieve the data using the transaction hash, ensuring secure and verifiable file authenticity.

## 📦 Features

- 🚀 Upload files to IPFS (InterPlanetary File System)
- 🔐 Generate SHA-256 hash of file data
- ⛓️ Record the hash into a custom-built blockchain ledger
- 🧾 Retrieve files based on the transaction hash
- 🧠 Simple CLI-based interface for interaction
- 📂 Log file for storing blockchain state persistently

## 🧰 Tech Stack

- **Python**: Core blockchain logic and IPFS integration
- **IPFS (via API or CLI)**: Decentralized file storage
- **SHA-256**: Hashing algorithm used for proof-of-integrity
- **JSON**: For data serialization and block structure

## 📁 Project Structure

```
.
├── blockchain.py           # Blockchain class with PoW logic
├── ipfs_integration.py     # Functions to upload/retrieve from IPFS
├── app.py                  # Main CLI script
├── ledger.json             # Stores the full blockchain
├── sample_files/           # Files to be uploaded
└── README.md
```

## ⚙️ How It Works

1. User uploads a file through CLI.
2. The file is sent to IPFS and a content-addressable hash is returned.
3. This hash is stored in a blockchain block with a timestamp and proof-of-work.
4. The user can retrieve and verify any file by providing the transaction hash.

## 📝 Sample Transaction (Blockchain Block)

```json
{
  "index": 5,
  "timestamp": "2025-07-18 14:23:12",
  "proof": 294834,
  "previous_hash": "0cc175b9c0f1b6a831c399e269772661",
  "data": {
    "ipfs_hash": "QmXYZ123...",
    "file_name": "project_report.pdf"
  }
}
```

## 🚀 Getting Started

1. **Install IPFS**  
   [Install IPFS](https://docs.ipfs.io/install/) and run a local daemon:
   ```bash
   ipfs daemon
   ```

2. **Clone and Run the Project**
   ```bash
   git clone https://github.com/yourusername/blockchain-ipfs-proof.git
   cd blockchain-ipfs-proof
   python app.py
   ```

3. **Upload a File**
   Follow the interactive CLI prompts to upload a file to IPFS and store its hash.

4. **Retrieve a File**
   Use the transaction hash to fetch the file back from IPFS and validate integrity.

## 🧪 Example Use Case

> Uploading a `contract.pdf` to IPFS, generating a unique hash, and storing it as an immutable record on the blockchain for legal verification.

## ✅ Future Enhancements

- 🔗 Smart contract integration (Ethereum/Solana)
- 🌐 Web interface for upload & validation
- 🛡️ Digital signature validation
- 📈 File verification analytics

---

🧠 **Built as part of a Blockchain + Decentralized Storage demo project**
