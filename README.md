# 🔐 Steganography & Encryption Suite (Java Desktop App)

A powerful Java-based desktop application that enables users to encrypt sensitive messages using a passkey and securely embed them into images or audio files using steganography techniques. It also provides a way to extract and decrypt hidden messages.

---

## ✨ Features

### 🔒 Encryption & Decryption
- **XOR + Base64 encryption** to obfuscate messages using a secret passkey.
- Ensures that even simple messages are not human-readable without the key.
- Encrypted messages are saved as `.txt` files for easy storage and sharing.

### 🖼️ Image Steganography
- Hide encrypted messages inside image files (`.png`, `.jpg`, `.jpeg`).
- Uses **Least Significant Bit (LSB)** technique to embed data without significantly altering the image visually.
- Extract hidden messages from stego images and decrypt them using the correct passkey.

### 🎵 Audio Steganography
- Hide encrypted messages inside `.wav` audio files.
- Maintain audio quality while concealing messages within digital samples.
- Extract and decrypt embedded messages from audio files.

### 🧑‍💻 Easy-to-Use GUI
- Built using Java Swing for a clean and intuitive interface.
- Includes buttons for each core action:
  - Encrypt Message
  - Decrypt Message
  - Encrypt & Hide in Image
  - Extract & Decrypt from Image
  - Encrypt & Hide in Audio
  - Extract & Decrypt from Audio
- Uses file choosers to help users select the desired media files.

### 📁 Organized Output
- All encrypted and stego media files are saved under a dedicated folder:
  - `src/main/input_output/`

### ⚠️ Validation & Error Handling
- Base64 validation ensures only valid encoded messages are decrypted.
- Informative error messages and confirmations using dialog boxes.
- Handles edge cases like empty input fields, invalid images/audio, or incorrect passkeys.

---

## 🧰 Technologies Used

- **Java 8+**
- **Java Swing** – for GUI
- **BufferedImage / ImageIO** – for image processing
- **Base64 Encoding** – for clean and safe encrypted output
- **WAV audio handling** – custom byte-level manipulation for audio steganography

---

## 🧪 Usage Instructions

### 🔐 Encrypt Message
- Click **"Encrypt Message"**
- Enter your message and passkey
- The encrypted text is saved to `src/main/input_output/encrypted_message.txt`

### 🔓 Decrypt Message
- Click **"Decrypt Message"**
- Select the encrypted `.txt` file and enter the passkey
- The decrypted message will be shown

### 🖼️ Encrypt & Hide in Image
- Click **"Encrypt & Hide in Image"**
- Enter message and passkey
- Choose an image file
- Result saved as `stego_image.png`

### 🔍 Extract & Decrypt from Image
- Click **"Extract & Decrypt from Image"**
- Select stego image
- Enter passkey to view hidden message

### 🎵 Encrypt & Hide in Audio
- Click **"Encrypt & Hide in Audio"**
- Enter message and passkey
- Select a `.wav` file
- Result saved as `stego_audio.wav`

### 🎧 Extract & Decrypt from Audio
- Click **"Extract & Decrypt from Audio"**
- Select stego audio file
- Enter passkey to view hidden message

---

## 🖼️ Screenshots

> _You can add screenshots here:_

- Main GUI Interface  
- Encrypt Message Dialog  
- File selection using `JFileChooser`  
- Message successfully hidden/extracted dialogs

---

## 📌 Notes & Limitations

- ❗ **XOR encryption is not secure** for real-world applications.
- 🎵 Audio steganography currently supports only `.wav` files.
- 📷 Make sure image/audio files are of **sufficient size** to hide the entire encrypted message.
