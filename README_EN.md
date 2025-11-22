# 🔮 Phantom Socket Premium v2.0

<div align="center">

![Python Version](https://img.shields.io/badge/python-3.6%2B-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20Termux-lightgrey.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

**Advanced Port Scanning and Security Analysis Tool**

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Examples](#-usage-examples) • [Warnings](#-important-warnings)

</div>

---

## 📋 Table of Contents

- [About](#-about)
- [Features](#-features)
- [System Requirements](#-system-requirements)
- [Installation](#-installation)
- [Usage](#-usage)
- [Usage Examples](#-usage-examples)
- [Scan Types](#-scan-types)
- [Important Warnings](#-important-warnings)
- [Legal Disclaimer](#-legal-disclaimer)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🔍 About

**Phantom Socket Premium** is a professional port scanning and security analysis tool developed for network security experts and system administrators. With advanced features and detailed reporting capabilities, it allows you to comprehensively analyze the security status of your systems.

### 🎯 Purpose

This tool has been developed for **educational and testing purposes**. It is designed to help system administrators and security researchers test their own systems.

---

## ✨ Features

### 🚀 Core Features

- **🔥 Fast Multi-threaded Scanning**: Support for up to 2000 concurrent threads
- **🎯 Advanced Service Recognition**: Detailed information for 50+ common services
- **🏷️ Banner Grabbing**: Service version and information gathering
- **📊 Detailed Risk Analysis**: Automatic security risk assessment
- **💾 JSON Export**: Save scan results in JSON format
- **🎨 Colored Terminal Output**: Easy to read and professional appearance

### 🔐 Security Features

- **Risk Level Determination**: Risk assessment for each port (Low, Medium, High, Critical)
- **Security Recommendations**: Detailed security advice based on ports
- **Category-Based Analysis**: Analyze services by categories
- **Comprehensive Reporting**: Generate detailed security reports

### 📈 Scan Modes

1. **Quick Scan**: Most common 21 ports
2. **Standard Scan**: Ports 1-1000 + critical ports
3. **Full Scan**: All ports (1-65535)
4. **Web Services**: HTTP/HTTPS ports
5. **Database Services**: Database ports
6. **Remote Access**: RDP, SSH, VNC, Telnet ports

---

## 💻 System Requirements

### Minimum Requirements

- **Operating System**: Linux, Termux (Android), macOS
- **Python**: 3.6 or higher
- **RAM**: 512 MB (recommended: 1 GB+)
- **Internet Connection**: Required

### Supported Platforms

| Platform | Status | Notes |
|----------|--------|-------|
| 🐧 Linux | ✅ Full Support | Ubuntu, Debian, Kali, Arch, etc. |
| 📱 Termux | ✅ Full Support | For Android devices |
| 🍎 macOS | ✅ Full Support | macOS 10.12+ |
| 🪟 Windows | ⚠️ Limited | WSL usage recommended |

---

## 📦 Installation

### Linux Installation

```bash
# Clone the repository
git clone https://github.com/Muhammedcengizz598/phantom-socket.git
cd phantom-socket

# Install required packages
pip3 install -r requirements.txt

# Give execution permission
chmod +x phantom_socket.py

# Run the tool
python3 phantom_socket.py
```

### Termux Installation (Android)

```bash
# Update Termux
pkg update && pkg upgrade

# Install Python and Git
pkg install python git

# Clone the repository
git clone https://github.com/Muhammedcengizz598/phantom-socket.git
cd phantom-socket

# Install required packages
pip install -r requirements.txt

# Run the tool
python phantom_socket.py
```

### Manual Installation

```bash
# Make sure Python 3 is installed
python3 --version

# Download the file
wget https://raw.githubusercontent.com/Muhammedcengizz598/phantom-socket/main/phantom_socket.py

# Run it
python3 phantom_socket.py
```

---

## 🎮 Usage

### Basic Usage

```bash
python3 phantom_socket.py
```

When the tool runs, it will ask you for the following information:

1. **Target Domain/IP**: The target you want to scan (e.g., example.com, 192.168.1.1)
2. **Scan Type**: Choose from 1-6 (default: Quick Scan)
3. **Export Option**: Do you want to save results as JSON? (y/n)
4. **Ethical Use Confirmation**: Confirm that you will only use the tool on your own systems

### Command Line Parameters

```bash
# Direct execution
python3 phantom_socket.py

# Run in background (Linux)
nohup python3 phantom_socket.py &

# Run with Screen
screen -S phantom python3 phantom_socket.py
```

---

## 📚 Usage Examples

### Example 1: Quick Scan

```bash
$ python3 phantom_socket.py

🎯 Enter target domain or IP address: example.com

📋 Select scan type:
1. Quick Scan (Common ports)
Your choice (1-6, default 1): 1

Do you want to export results to JSON file? (y/n): y

Do you confirm you will only use this tool on your own systems? (y/n): y
```

### Example 2: Web Services Scan

```bash
$ python3 phantom_socket.py

🎯 Enter target domain or IP address: 192.168.1.100

📋 Select scan type:
4. Web Services
Your choice (1-6, default 1): 4

Do you want to export results to JSON file? (y/n): n

Do you confirm you will only use this tool on your own systems? (y/n): y
```

### Example 3: Full Port Scan

```bash
$ python3 phantom_socket.py

🎯 Enter target domain or IP address: localhost

📋 Select scan type:
3. Full Scan (1-65535)
Your choice (1-6, default 1): 3

Do you want to export results to JSON file? (y/n): y

Do you confirm you will only use this tool on your own systems? (y/n): y
```

---

## 🎯 Scan Types

### 1️⃣ Quick Scan

**Scan Duration**: ~10-30 seconds  
**Number of Ports**: 21 ports  
**Use Case**: Quick security check

**Scanned Ports**:
- Web: 80, 443, 8080
- FTP: 21
- SSH: 22
- Telnet: 23
- Email: 25, 110, 143, 993, 995
- DNS: 53
- Windows: 135, 139, 445
- Database: 1433, 3306, 5432, 6379, 27017
- Remote Access: 3389, 5900

### 2️⃣ Standard Scan

**Scan Duration**: ~2-5 minutes  
**Number of Ports**: 1000+ ports  
**Use Case**: Comprehensive security analysis

### 3️⃣ Full Scan

**Scan Duration**: ~10-30 minutes  
**Number of Ports**: 65535 ports  
**Use Case**: Detailed penetration testing

### 4️⃣ Web Services

**Scan Duration**: ~5-10 seconds  
**Number of Ports**: 8 ports  
**Use Case**: Web server security check

### 5️⃣ Database Services

**Scan Duration**: ~5-10 seconds  
**Number of Ports**: 7 ports  
**Use Case**: Database security check

### 6️⃣ Remote Access Services

**Scan Duration**: ~5-10 seconds  
**Number of Ports**: 6 ports  
**Use Case**: Remote access security check

---

## ⚠️ Important Warnings

### 🚨 Ethical Use

> **WARNING**: This tool has been developed for **educational and testing purposes only**.

#### ✅ Permitted Uses

- ✔️ Testing your own systems
- ✔️ Scanning systems you have permission to scan
- ✔️ Educational use in laboratory environments
- ✔️ Security research (within legal framework)
- ✔️ Penetration testing (with written permission)

#### ❌ Prohibited Uses

- ❌ Scanning systems without permission
- ❌ Malicious use
- ❌ Illegal activities
- ❌ Harming other people's systems
- ❌ Unauthorized access attempts

### 🔒 Security Notes

1. **VPN Usage**: It is recommended to use a VPN even when scanning your own systems
2. **Permission Letter**: Always obtain written permission for corporate systems
3. **Log Records**: Keep records of all your scanning activities
4. **Responsibility**: All responsibility for the use of this tool lies with the user

### 📜 Legal Disclaimer

```
⚖️ LEGAL LIABILITY DISCLAIMER

This tool has been developed for testing computer network security and 
educational purposes. All legal responsibility arising from the use of 
this tool lies with the user.

The developers (Muhammed Cengiz and contributors) cannot be held 
responsible for misuse of this tool, illegal activities, or any damage 
caused by it.

By using this tool, you agree to use it only within legal and ethical 
frameworks.
```

---

## 📊 Output Formats

### Terminal Output

The tool provides colored and detailed terminal output:

- 🟢 **Green**: Successful operations and low-risk ports
- 🟡 **Yellow**: Warnings and medium-risk ports
- 🟠 **Orange**: High-risk ports
- 🔴 **Red**: Critical-risk ports and errors
- 🔵 **Blue**: Informational messages

### JSON Export

Scan results can be saved in JSON format:

```json
{
  "scan_info": {
    "target": "example.com",
    "scan_time": "2024-01-15T10:30:00",
    "duration": 45.23,
    "total_ports_scanned": 1021
  },
  "results": {
    "open_ports": 5,
    "closed_ports": 1015,
    "filtered_ports": 1
  },
  "detailed_results": {
    "80": {
      "port": 80,
      "status": "open",
      "service": "HTTP",
      "risk": "MEDIUM",
      "banner": "Apache/2.4.41"
    }
  }
}
```

---

## 🛠️ Troubleshooting

### Common Errors and Solutions

#### Error: "Permission Denied"

```bash
# Solution: Run with root privileges
sudo python3 phantom_socket.py
```

#### Error: "Module not found"

```bash
# Solution: Reinstall requirements
pip3 install -r requirements.txt --upgrade
```

#### Error: "Connection timeout"

```bash
# Solution: Increase timeout or use fewer threads
# Increase socket.settimeout() value in the code
```

#### Error: "Too many open files"

```bash
# Linux solution:
ulimit -n 4096

# Termux solution:
# Reduce the number of threads (decrease max_threads value in code)
```

---

## 🤝 Contributing

If you want to contribute to the project:

1. Fork the project
2. Create a new branch (`git checkout -b feature/newFeature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push your branch (`git push origin feature/newFeature`)
5. Create a Pull Request

### Contribution Guidelines

- ✅ Write clean and readable code
- ✅ Add comments
- ✅ Test your changes
- ✅ Update documentation
- ✅ Follow ethical use principles

---

## 📝 Changelog

### v2.0 (Current)
- ✨ Advanced service recognition system
- ✨ Banner grabbing feature
- ✨ JSON export support
- ✨ Risk analysis and security recommendations
- ✨ Category-based port analysis
- ✨ Multiple scan modes
- 🐛 Performance improvements

### v1.0
- 🎉 Initial release
- ⚡ Basic port scanning
- 🎨 Colored terminal output

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 Muhammed Cengiz

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Developer

**Muhammed Cengiz**

- 🌐 GitHub: [@Muhammedcengizz598](https://github.com/Muhammedcengizz598)
- 📧 Email: [Visit GitHub profile for contact]
- 💼 LinkedIn: [Your profile link]

---

## 🌟 Thank You

Thank you for using this project! If you found it useful:

- ⭐ Star the project
- 🐛 Report bugs
- 💡 Make suggestions
- 🤝 Contribute

---

## 📞 Contact and Support

### Support Channels

- 🐛 **Bug Reports**: [GitHub Issues](https://github.com/Muhammedcengizz598/phantom-socket/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/Muhammedcengizz598/phantom-socket/discussions)
- 📧 **Email**: Contact via GitHub profile

### Frequently Asked Questions (FAQ)

**Q: Is this tool legal?**  
A: Yes, it is legal to use on your own systems or systems you have permission to scan.

**Q: Does it work on Termux?**  
A: Yes, it works seamlessly on Termux. Follow the installation instructions.

**Q: Do I need root privileges?**  
A: Root privileges may be required to scan certain ports.

**Q: How many ports can I scan?**  
A: In full scan mode, you can scan up to 65535 ports.

**Q: How can I save the results?**  
A: You can save results using the JSON export feature.

---

## 🔗 Useful Links

- 📚 [Python Documentation](https://docs.python.org/3/)
- 🔒 [OWASP Port Scanning](https://owasp.org/www-community/vulnerabilities/Port_scanning)
- 🛡️ [Nmap Reference](https://nmap.org/book/man.html)
- 📖 [Cybersecurity Resources](https://www.cybrary.it/)

---

<div align="center">

### 🌟 Don't Forget to Star the Project if You Like It! 🌟

**Phantom Socket Premium v2.0**

*Happy secure scanning!* 🔐

---

**© 2024 Muhammed Cengiz | All Rights Reserved**

*This tool is for educational purposes. Use responsibly and ethically.*

</div>
