

Name : ABIDASS k <br>
Company: CODTECH IT SOLUTIONS <br>
Intern ID : CT08DS6417 <br>
Domain : CYBER SECURITY&ETHICAL HACKING <br>
Duration: Augest to September 2024 <br>
Mentor : Muzammil Ahmed <br>
# Vulnerability Scanning Tool
<img src="https://github.com/Abidasskumar/CODTECH-TASK1/blob/main/open%20port%20output%20image.png">
## Overview
This tool leverages Nmap to scan for open ports on a target system and includes a Python script to identify outdated software. The tool is essential for security professionals to assess and mitigate vulnerabilities.

## Prerequisites
- **Nmap**: Ensure Nmap is installed on your system. You can install it via:
  ```bash
  sudo apt-get install nmap  # Debian/Ubuntu
  brew install nmap          # macOS
  ```
- **Python 3.x**: Ensure Python is installed. You can check by running:
  ```bash
  python3 --version
  ```

## Nmap Usage: Finding Open Ports

Use the following command to scan for open ports on a target IP or hostname:

```bash
nmap -sS -p 1-65535 <target-ip>
```

- **-sS**: Performs a TCP SYN scan.
- **-p 1-65535**: Scans all ports (1 through 65535).

### Example:
```bash
nmap -sS -p 1-65535 192.168.1.1
```
 


## Python Script: Finding Outdated Software

This script checks installed Python packages against the latest available versions on PyPI, identifying any outdated software.

### Installation:
```bash
pip install pip-review
```

### Script:
```python
import subprocess

def find_outdated_packages():
    result = subprocess.run(['pip-review', '--outdated'], capture_output=True, text=True)
    if result.stdout:
        print("Outdated Packages:")
        print(result.stdout)
    else:
        print("All packages are up to date.")

if __name__ == "__main__":
    find_outdated_packages()
```

<img src="https://github.com/Abidasskumar/CODTECH-TASK1/blob/main/Outdated%20Software%20Checking%20Output%20Image">

### Usage:
1. Run the script using Python:
   ```bash
   python3 outdated_software.py
   ```
2. The script will output a list of outdated packages,
 


## License
This tool is released under the MIT License. See [LICENSE](LICENSE) for more information.

