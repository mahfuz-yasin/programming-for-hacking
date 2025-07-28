
# 📘 Lesson 13: Modules & Packages

Python-এ কোডকে ছোট ছোট অংশে ভাগ করে ব্যবহারযোগ্য ও পুনরায় ব্যবহারযোগ্য করা হয় **Modules** এবং **Packages** ব্যবহার করে। এটি বড় প্রজেক্টে কোড সংগঠনে সাহায্য করে।

---

## 📦 1. `import` ও `from-import`

### 📌 কি?

Python-এর অন্য ফাইল বা মডিউল থেকে ফাংশন/ভেরিয়েবল/ক্লাস ইত্যাদি ব্যবহার করতে চাইলে `import` বা `from ... import ...` ব্যবহার করা হয়।

### 📌 কেন ব্যবহার হয়?

* কোড রিইউজ করতে
* Python-এর বিল্ট-ইন বা থার্ড পার্টি মডিউল ব্যবহার করতে
* প্রজেক্টের কোডকে আলাদা ফাইলে ভাগ করে সংগঠিত করতে

### 📌 কোথায় ব্যবহার হয়?

* ফাইল ম্যানিপুলেশন (`os`)
* ম্যাথমেটিক্স ও এলগরিদম (`math`)
* ডেট ও টাইম কাজ (`datetime`)
* র‍্যান্ডম সিস্টেমে (`random`)

### ✅ Example:

```python
import math
print(math.sqrt(16))  # Output: 4.0

from datetime import date
print(date.today())   # Output: 2025-07-28 (উদাহরণ)
```

---

## 🧰 2. Built-in Modules: `os`, `sys`, `math`, `random`, `datetime`

### 🔹 `os` → Operating system এর সাথে interaction

```python
import os
print(os.getcwd())        # বর্তমান ডিরেক্টরি
os.mkdir("new_folder")    # নতুন ফোল্ডার তৈরি
```

### 🔹 `sys` → Python interpreter সংক্রান্ত

```python
import sys
print(sys.version)        # Python version
print(sys.argv)           # কমান্ড লাইন আর্গুমেন্ট
```

### 🔹 `math` → ম্যাথমেটিক্যাল ফাংশন

```python
import math
print(math.factorial(5))  # 120
print(math.pi)            # 3.1415...
```

### 🔹 `random` → র‍্যান্ডম নম্বর/চয়েজ

```python
import random
print(random.randint(1, 10))   # ১ থেকে ১০ এর মধ্যে র‍্যান্ডম সংখ্যা
```

### 🔹 `datetime` → সময় ও তারিখ নিয়ে কাজ

```python
from datetime import datetime
now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M:%S"))
```

---

## 🛠️ 3. Creating and Using Custom Modules

### 📌 কি?

নিজের Python ফাইল (যেমন `utils.py`) কে অন্য প্রজেক্টে মডিউল হিসেবে ব্যবহার করা।

### ✅ Example:

#### 👉 `utils.py`

```python
def greet(name):
    return f"Hello, {name}!"
```

#### 👉 `main.py`

```python
import utils
print(utils.greet("Mahfuz"))
```

### 📌 কেন ব্যবহার হয়?

* নিজস্ব ফাংশন ও ক্লাসকে বারবার ব্যবহার করার জন্য
* প্রজেক্টের কোড মডিউলার ও পরিচ্ছন্ন রাখতে

### 📌 কোথায় ব্যবহার হয়?

* রিইউজেবল ফাংশন, টুল, কনফিগারেশন ফাইল ইত্যাদি

---

## 🧠 4. `__pycache__` এবং `.pyc` ফাইল কী?

### 📌 কি?

Python যখন কোনো মডিউল রান করে, তখন `.pyc` (compiled bytecode) ফাইল তৈরি করে এবং তা `__pycache__` ফোল্ডারে জমা রাখে।

### 📌 কেন ব্যবহার হয়?

* পরবর্তীতে একই মডিউল রান করলে execution time কম হয়।
* Performance optimization

### 📌 কোথায় দেখা যায়?

* যেকোনো Python প্রজেক্টের ডিরেক্টরিতে যেটি module ইমপোর্ট করে

---

## 🧪 Practice Exercises

1. `math` মডিউল ব্যবহার করে √২৫ বের করো।
2. `random` দিয়ে একটি র‍্যান্ডম নাম্বার প্রিন্ট করো ১ থেকে ১০ এর মধ্যে।
3. নিজের একটি `utils.py` তৈরি করো এবং সেটিকে অন্য ফাইলে `import` করো।
4. `os` ব্যবহার করে একটি ফোল্ডার তৈরি করো এবং তার নাম প্রিন্ট করো।
5. Python রান করার পর `__pycache__` ফোল্ডার কোথায় তৈরি হচ্ছে তা খুঁজে দেখো।

---

## 🧠 Summary

| বিষয়                                      | কাজ                                 |
| ----------------------------------------- | ----------------------------------- |
| `import`                                  | অন্য মডিউল ইমপোর্ট করতে             |
| `os`, `sys`, `math`, `random`, `datetime` | গুরুত্বপূর্ণ Python built-in মডিউল  |
| Custom Modules                            | নিজের কোড রিইউজ করার জন্য           |
| `__pycache__`                             | কম্পাইলড `.pyc` ফাইল সংরক্ষণের জন্য |
