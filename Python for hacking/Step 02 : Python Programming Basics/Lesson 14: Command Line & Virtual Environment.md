
# 📘 Lesson 14: Command Line & Virtual Environment

Python প্রজেক্ট তৈরি ও পরিচালনার ক্ষেত্রে **Command Line**, **Virtual Environment**, এবং **Package Management** গুরুত্বপূর্ণ ভূমিকা পালন করে। এই অধ্যায়ে আমরা শিখবো কীভাবে টার্মিনালে Python চালাতে হয়, কীভাবে ভার্চুয়াল এনভায়রনমেন্ট তৈরি করতে হয়, এবং প্যাকেজ ম্যানেজ করতে হয় `pip` দিয়ে।

---

## 🖥️ 1. Command-line Arguments (`sys.argv`)

### 📌 কি?

Python স্ক্রিপ্ট চালানোর সময় আমরা বাইরের থেকে যে ইনপুট দেই, তা **Command-line Arguments** নামে পরিচিত, এবং `sys.argv` দিয়ে access করা হয়।

### 📌 কেন?

* ইউজার ইনপুট ছাড়াই বাইরের data বা অপশন দিতে
* একাধিক ভ্যারিয়েবল dynamic ভাবে স্ক্রিপ্টে ব্যবহার করতে

### 📌 কোথায় ব্যবহার হয়?

* CLI tools
* Automation scripts
* Python প্রজেক্টে run-time কাস্টমাইজেশন

### ✅ Example:

```python
# save as hello.py
import sys
print("Hello", sys.argv[1])
```

```bash
$ python hello.py Mahfuz
Hello Mahfuz
```

➡️ `sys.argv[0]` = স্ক্রিপ্টের নাম, `sys.argv[1]` = প্রথম argument

---

## 🌐 2. Creating and Using Virtual Environments (`venv`)

### 📌 কি?

**Virtual Environment** হলো একধরনের আলাদা Python পরিবেশ যেখানে নির্দিষ্ট Python ভার্সন ও লাইব্রেরি থাকে — যা সিস্টেমের মূল Python সেটআপ থেকে আলাদা।

### 📌 কেন?

* Dependency conflict এড়াতে
* প্রতিটি প্রজেক্টে আলাদা লাইব্রেরি/ভার্সন ব্যবহারে স্বাধীনতা দিতে

### 📌 কোথায় ব্যবহার হয়?

* Django বা Flask ওয়েব অ্যাপ্লিকেশনে
* প্যাকেজ ডেভেলপমেন্ট
* বিভিন্ন Python ভার্সন সাপোর্টের জন্য

### ✅ তৈরি ও ব্যবহার:

```bash
# Virtual Environment তৈরি
python -m venv venv_folder_name

# Activate (Windows)
venv_folder_name\Scripts\activate

# Activate (Linux/macOS)
source venv_folder_name/bin/activate

# Deactivate
deactivate
```

---

## 📦 3. pip and Package Management

### 📌 কি?

**`pip`** হলো Python-এর official package installer। এটি দিয়ে আপনি লাইব্রেরি ইনস্টল, আনইনস্টল, ও আপডেট করতে পারেন।

### 📌 কেন?

* প্রয়োজনীয় লাইব্রেরি (যেমন `requests`, `numpy`, `flask`) ইনস্টল করতে
* প্রজেক্টের সকল ডিপেন্ডেন্সি ম্যানেজ করতে

### 📌 কোথায় ব্যবহার হয়?

* যেকোনো Python প্রজেক্টে থার্ড-পার্টি লাইব্রেরি ব্যবহারের সময়

### ✅ Common Commands:

```bash
pip install package_name         # লাইব্রেরি ইনস্টল
pip uninstall package_name       # আনইনস্টল
pip freeze > requirements.txt    # সকল লাইব্রেরির লিস্ট ফাইল তৈরি
pip install -r requirements.txt  # লিস্ট অনুযায়ী ইনস্টল
```

---

## ⚙️ 4. Python Shell Commands and Tricks

### 📌 কি?

Python Shell/Interpreter এ সরাসরি কোড চালানোর জন্য ব্যবহৃত হয়। এটি Quick Testing বা debugging এর জন্য কাজে আসে।

### ✅ শুরু করতে:

```bash
python
```

### 🛠️ Shell Tricks:

```python
>>> 5 + 3
8

>>> import math
>>> math.sqrt(16)
4.0

>>> help(str)  # স্ট্রিং ক্লাসের সমস্ত method ও description দেখাবে

>>> dir(list)  # লিস্টের সকল attributes ও methods দেখাবে
```

### 📌 কোথায় ব্যবহার হয়?

* দ্রুত কোনো ধারণা যাচাই করতে
* শেখার সময় রিয়েল টাইম output দেখতে

---

## 🧪 Practice Exercises

1. `sys.argv` ব্যবহার করে ২টি সংখ্যা ইনপুট নিয়ে যোগফল বের করো।
2. নতুন একটি virtual environment তৈরি করো এবং তাতে `requests` লাইব্রেরি ইনস্টল করো।
3. একটি `requirements.txt` ফাইল তৈরি করে সেটি ব্যবহার করে ইনস্টল করো।
4. Python shell-এ `math` মডিউলের `pow()` এবং `sqrt()` ফাংশন ব্যবহার করে দেখো।

---

## 🧠 Summary

| বিষয়         | কি করে                            |
| ------------ | --------------------------------- |
| `sys.argv`   | Command line ইনপুট নেয়            |
| `venv`       | আলাদা Python environment তৈরি করে |
| `pip`        | লাইব্রেরি install/manage করে      |
| Python Shell | সরাসরি কোড রান/পরীক্ষা করতে       |
