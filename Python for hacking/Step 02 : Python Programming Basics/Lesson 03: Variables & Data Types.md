
# 📘 Lesson 03: Variables & Data Types

Python-এ ভেরিয়েবল এবং ডেটা টাইপ হলো প্রোগ্রামিংয়ের ভিত্তি। এই অধ্যায়ে আমরা শিখবো কীভাবে ভেরিয়েবল তৈরি করা হয়, কী কী ডেটা টাইপ রয়েছে, কিভাবে টাইপ কনভার্ট করতে হয় এবং Python-এ কিছু ইনবিল্ট ফাংশন।

---

## 🧮 1. Variables and Naming Rules

### 🔹 What is a Variable?
ভেরিয়েবল হলো একটি **নাম** যার মাধ্যমে আমরা মেমোরিতে সংরক্ষিত কোনো মানকে (value) অ্যাক্সেস করি।

```python
x = 10
name = "Alice"
````

এখানে `x` এবং `name` হলো ভেরিয়েবল, আর `10` এবং `"Alice"` হলো তাদের মান।

### 📏 Naming Rules (PEP 8 অনুযায়ী):

* নাম অবশ্যই **letter (a-z, A-Z)** অথবা **underscore `_`** দিয়ে শুরু হবে।
* নামের মধ্যে **সংখ্যা** থাকতে পারে, কিন্তু শুরুতে নয়।
* **কোনো স্পেস** বা **special character (!, @, %, etc.)** ব্যবহার করা যাবে না।
* **কেস সেনসিটিভ**: `Name` এবং `name` আলাদা ভেরিয়েবল।
* Python-এর **keywords (if, else, class)** ভেরিয়েবল হিসেবে ব্যবহার করা যাবে না।

### ✅ ভালো উদাহরণ:

```python
user_name = "Mahfuz"
age = 25
```

### ❌ খারাপ উদাহরণ:

```python
2name = "John"      # Invalid: starts with number
user-name = "Ali"   # Invalid: contains dash
class = "Math"      # Invalid: keyword used
```

---

## 🔢 2. Data Types in Python

Python একটি **dynamically typed** language। মান (value) অনুযায়ী ভেরিয়েবলের টাইপ নির্ধারিত হয়।

### 🧾 Built-in Basic Types:

| Data Type  | Description       | Example           |
| ---------- | ----------------- | ----------------- |
| `int`      | পূর্ণসংখ্যা       | `x = 10`          |
| `float`    | দশমিক সংখ্যা      | `pi = 3.14`       |
| `str`      | স্ট্রিং বা টেক্সট | `name = "Ali"`    |
| `bool`     | সত্য/মিথ্যা       | `is_admin = True` |
| `NoneType` | শূন্য মান (Null)  | `value = None`    |

### 🧪 উদাহরণ:

```python
x = 100               # int
pi = 3.1416           # float
name = "Python"       # str
is_active = False     # bool
result = None         # NoneType
```

---

## 🔁 3. Type Casting (Type Conversion)

Python-এ ডেটার টাইপ পরিবর্তনের জন্য ব্যবহার হয় **type casting**।

### ✅ Common Casting Functions:

* `int()` → পূর্ণসংখ্যায় রূপান্তর
* `float()` → দশমিক সংখ্যায় রূপান্তর
* `str()` → স্ট্রিংয়ে রূপান্তর
* `bool()` → True/False এ রূপান্তর

### 🔄 উদাহরণ:

```python
x = int("5")           # "5" → 5
y = float(10)          # 10 → 10.0
z = str(3.14)          # 3.14 → "3.14"
b = bool(0)            # 0 → False
```

### 🔎 Practical Case:

```python
user_input = "25"
total = int(user_input) + 5
print(total)  # Output: 30
```

---

## 🔍 4. Built-in Functions: `type()`, `isinstance()`, `id()`

### 📌 `type()`: কোনো ভেরিয়েবলের ডেটা টাইপ চেক করতে

```python
x = 5
print(type(x))  # <class 'int'>
```

### 📌 `isinstance()`: কোনো ভেরিয়েবল নির্দিষ্ট টাইপের কি না যাচাই করতে

```python
print(isinstance(x, int))      # True
print(isinstance(x, float))    # False
```

### 📌 `id()`: ভেরিয়েবলের মেমোরি ঠিকানা দেখতে

```python
a = 10
b = 10
print(id(a))     # Example: 140710567438304
print(id(b))     # Python may store same ID for small immutable ints
```

---

## ✅ Summary

* ভেরিয়েবল হলো একটি নাম, যা মান ধারণ করে।
* Python-এ অনেক ধরণের ডেটা টাইপ রয়েছে: `int`, `float`, `str`, `bool`, `None`
* `type()`, `isinstance()`, `id()` — ডেটা বিশ্লেষণের জন্য গুরুত্বপূর্ণ ফাংশন।
* টাইপ কাস্টিং ব্যবহার করে ডেটা এক টাইপ থেকে আরেক টাইপে রূপান্তর করা যায়।

---