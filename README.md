# Set Validator Metadata and Node Image

This script helps you upload your validator's metadata and image to IPFS, then update the StakeManager contract on Polygon with the new metadata URI.

---

## 🚀 Prerequisites

- **Validator private key from file**: `./test-chain-5/consensus/validator.key`
- **Polygon funds**: Some $POL (MATIC) in the validator wallet

## 🛠 Technical Requirements

- **Node.js**: v18.20.x  
- **npm**

## 📦 Installation

1. Switch to Node 18  
    nvm use 18

2. Configure environment  
    - Update the `.env` file in the project root
    - Set your Polygon RPC endpoint (or use the default public RPC provided)

3. Add your validator image  
    - Place a `PNG` image (256×256px) in this directory alongside the script  
    - Example: `my-logo.png`

4. Install dependencies  
    npm install

---

## ▶️ Usage

Run the `updateValidatorInfo.js` script with the following arguments:

    node updateValidatorInfo.js <VALIDATOR_PRIVATE_KEY> "<VALIDATOR_NAME>" "<METADATA_JSON_OR_EMPTY>" <PATH_TO_VALIDATOR_IMAGE>

- `<VALIDATOR_PRIVATE_KEY>`: Your node's private key (hex string)  
- `<VALIDATOR_NAME>`: A descriptive name for your validator (wrapped in quotes)  
- `<METADATA_JSON_OR_EMPTY>`: Any additional metadata as a JSON string, or `" "` for none  
- `<PATH_TO_VALIDATOR_IMAGE>`: Path to your 256×256 PNG image  

### Example

    node updateValidatorInfo.js c9617b2f1dabf9f5501eba795008f587ecab164aeb31217a7b76448d62157209 "My Validator Node" " " ./my-logo.png

---

## 📄 License

This project is licensed under the MIT License. Feel free to use and modify it as you see fit.
