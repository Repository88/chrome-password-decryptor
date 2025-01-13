# Chrome Password Decryptor

A Python utility to safely decrypt and export saved passwords from Chrome, Edge, Brave, and Firefox browsers.

## 🔑 Features

- Extract saved passwords from multiple browsers:
  - Google Chrome
  - Microsoft Edge
  - Brave Browser
  - Mozilla Firefox
- Cross-platform support (Windows, macOS, Linux)
- Multi-profile support
- Export to CSV or JSON
- Secure local decryption
- Command-line interface

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/kiryano/chrome-password-decryptor.git
cd chrome-password-decryptor

# Install requirements
pip install -r requirements.txt

# Run the decryptor
python decrypt.py
```

## 📋 Requirements

- Python 3.8+
- pycryptodomex
- colorama
- pywin32 (Windows only)
- libnss (Linux only, for Firefox)

## 💻 Usage

Basic usage:
```bash
python decrypt.py
```

Advanced options:
```bash
# Decrypt from all supported browsers
python decrypt.py -b chrome edge brave firefox

# Export as JSON
python decrypt.py -f json -o passwords.json

# Quiet mode
python decrypt.py -q
```

### Command Line Options

```
-b, --browsers    Specify browsers (default: chrome)
-f, --format      Output format: csv/json (default: csv)
-o, --output      Output filename (default: passwords.csv)
-q, --quiet       Silent mode
```

## 🛠️ Troubleshooting

### Windows
If you get permission errors:
```powershell
# Run as administrator
Start-Process python -ArgumentList "decrypt.py" -Verb RunAs
```

### Linux/Mac
```bash
# Fix permissions
chmod +x decrypt.py
sudo python decrypt.py
```

## 🔒 Security

- Local decryption only - no network access
- Automatic cleanup of temporary files
- Uses system keyring for secure key handling
- Password files (.csv, .json) excluded from git

## 📝 License

MIT License

## ⚠️ Disclaimer

This tool is for educational purposes and personal use only. Users are responsible for compliance with applicable laws and regulations.

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📌 Todo

- [ ] Add Firefox support for macOS
- [ ] Implement password strength analysis
- [ ] Add GUI interface
- [ ] Add tests
- [ ] Add CI/CD pipeline
