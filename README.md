# Change Your IP and Location

A powerful script that automatically changes your IP address and location every 3 seconds. 

⚠️ **NOTICE**: This tool is intended **ONLY for educational purposes and laboratory testing**. Misuse of this tool for illegal or malicious purposes is strictly prohibited. The author is not responsible for any misuse.

## Features
- 🔄 Automatic IP rotation every 3 seconds
- 📍 Location spoofing capabilities
- 🛡️ Lightweight and efficient
- 🔧 Easy to use and configure

---

## Mandatory Requirements

### Packages Required:
- **Python 3.7+** or higher
- **pip** (Python package manager)
- **requests** - for making HTTP requests
- **tor** - for IP rotation (optional but recommended)
- **curl** - for testing IP changes

### System Requirements:
- Linux-based operating system (Ubuntu, Debian, Kali Linux, etc.)
- Sudo/Administrator access (for some operations)
- Stable internet connection

---

## Installation

### Step 1: Clone the Repository
```bash
git clone https://github.com/Linuxlabpro/Change-your-ip-and-location-.git
cd Change-your-ip-and-location-
```

### Step 2: Install Mandatory Dependencies

#### For Debian/Ubuntu-based Systems:
```bash
sudo apt-get update
sudo apt-get install python3 python3-pip tor curl -y
```

#### For Fedora/RedHat-based Systems:
```bash
sudo dnf install python3 python3-pip tor curl -y
```

#### For Arch Linux:
```bash
sudo pacman -S python python-pip tor curl
```

### Step 3: Install Python Dependencies
```bash
pip3 install -r requirements.txt
```

---

## Usage

### Basic Run Command:
```bash
python3 script.py
```

### With Verbose Output:
```bash
python3 script.py -v
```

### With Custom Interval (in seconds):
```bash
python3 script.py --interval 3
```

### Run as Background Process:
```bash
nohup python3 script.py > ip_change.log 2>&1 &
```

### Stop the Script:
```bash
pkill -f "python3 script.py"
```

---

## Requirements.txt

Create a `requirements.txt` file with the following mandatory packages:

```txt
requests==2.31.0
stem==1.8.2
pysocks==1.7.1
beautifulsoup4==4.12.2
```

---

## How It Works

1. The script connects to Tor network for IP rotation
2. Every 3 seconds, a new exit node is used (changing your IP and apparent location)
3. Your actual IP and location are masked
4. Continuous rotation provides privacy during your lab testing

---

## Testing

Check your IP and location changes:

```bash
# Terminal 1: Run the script
python3 script.py

# Terminal 2: Check your current IP
curl https://api.ipify.org?format=json
curl https://ipapi.co/json/
```

You should see different IPs every 3 seconds.

---

## Important Notes

⚠️ **Disclaimer:**
- For **laboratory and light testing purposes only**
- Do **NOT** use for illegal activities
- Do **NOT** use for bypassing security systems maliciously
- Do **NOT** use for evading detection in unauthorized systems
- Users are responsible for complying with all local, state, and national laws

---

## Troubleshooting

### Issue: Tor Connection Failed
```bash
sudo service tor start
sudo service tor status
```

### Issue: Permission Denied
```bash
chmod +x script.py
sudo python3 script.py
```

### Issue: Packages Not Found
```bash
pip3 install --upgrade pip
pip3 install -r requirements.txt
```

---

## Support & Contact

For issues or questions, please open an issue on the repository.

---

## License

Educational Use Only - See LICENSE file

---

**Happy Testing! 🚀**

*Remember: With great power comes great responsibility. Use this tool ethically and legally.*
