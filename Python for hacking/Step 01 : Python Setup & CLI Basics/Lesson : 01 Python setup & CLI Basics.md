
**Python Setup & CLI Basics**  **Windows, Linux, Ubuntu, Kali Linux, এবং macOS**-এ — হ্যাকিংয়ের উদ্দেশ্যে।


# 🛠️ Step 01: Python Setup & CLI Basics (for Ethical Hacking)

## 🪟 **Windows (10/11)**

### ✅ 1. Python Install:

* Go to: [https://python.org/downloads](https://python.org/downloads)
* Download latest version (e.g. 3.12.x)
* Installer চালান এবং ✅ **"Add Python to PATH"** চেকবক্স টিক দিন
* Click: Install Now

### ✅ 2. Verify:

```bash
    python --version
    pip --version
```

### ✅ 3. Recommended CLI Tools:

* **Terminal:** Windows PowerShell বা Windows Terminal
* **Optional:** Git Bash, Cmder, or install WSL (for Linux-like environment)

---

## 🐧 **Linux (Generic: Fedora, Arch, etc.)**

### ✅ 1. Check Python:

```bash
    python3 --version
```

> বেশিরভাগ Linux ডিস্ট্রোতে Python 3 pre-installed থাকে।

### ✅ 2. Install if not present:

```bash
sudo apt install python3 python3-pip -y      # For Debian/Ubuntu-based
sudo dnf install python3 -y                   # For Fedora
```

### ✅ 3. Check:

```bash
which python3
pip3 --version
```

---

## 🧱 **Ubuntu (Desktop/Server)**

> Ubuntu-তে Python 3 pre-installed থাকে।

### ✅ 1. Update & Upgrade:

```bash
sudo apt update && sudo apt upgrade -y
```

### ✅ 2. Install pip & essential tools:

```bash
sudo apt install python3-pip python3-venv -y
```

### ✅ 3. Check:

```bash
python3 --version
pip3 --version
```

### ✅ 4. Create Test File:

```bash
nano hello.py
# Paste: print("Hello Hacker!")
python3 hello.py
```

---

## 🕵️‍♂️ **Kali Linux (Hacker’s OS)**

> Kali-তে Python 3 ও pip pre-installed থাকে।

### ✅ 1. Update & Install Essentials:

```bash
sudo apt update && sudo apt install python3 python3-pip python3-venv -y
```

### ✅ 2. Verify:

```bash
python3 --version
pip3 --version
```

### ✅ 3. Optional Tools for Hacking:

```bash
pip3 install scapy requests colorama
```

---

## 🍎 **macOS (Intel / M1 / M2)**

### ✅ 1. Install Homebrew (if not already):

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### ✅ 2. Install Python 3:

```bash
brew install python
```

### ✅ 3. Verify:

```bash
python3 --version
pip3 --version
```

### ✅ 4. Create a Script:

```bash
nano hello.py
# print("Hello macOS Hacker!")
python3 hello.py
```

---

## 🔁 Common CLI Basics (For All OS)

| Command                   | কাজ                     |
| ------------------------- | ----------------------- |
| `cd foldername`           | ফোল্ডারে ঢোকা           |
| `ls` / `dir`              | ফোল্ডারের ভেতর দেখতে    |
| `mkdir myfolder`          | নতুন ফোল্ডার তৈরি       |
| `touch file.py`           | ফাইল তৈরি (Linux/mac)   |
| `python3 file.py`         | Python ফাইল চালানো      |
| `pip install module-name` | Python লাইব্রেরি ইন্সটল |
| `clear` / `cls`           | টার্মিনাল পরিষ্কার      |

---

## ✅ Recommended Tools After Setup:

* ✅ `VS Code` (code editor): [https://code.visualstudio.com](https://code.visualstudio.com)
* ✅ `Python Extension` in VS Code
* ✅ `Git` & `GitHub CLI` for version control

---

## 📦 Example Test Script:

```python
# test.py
import os
print("Welcome, Ethical Hacker!")
print("Your current path is:", os.getcwd())
```

Run with:

```bash
python3 test.py
```
