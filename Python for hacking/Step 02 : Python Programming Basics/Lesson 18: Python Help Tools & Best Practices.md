
# 📘 Lesson 18: Python Help Tools & Best Practices

Python শেখার পাশাপাশি তার built-in **সহায়ক টুল**, **কোড লেখার নিয়ম (PEP 8)** এবং **ডিবাগিং দক্ষতা** জানা একজন প্রোগ্রামারের জন্য অত্যন্ত গুরুত্বপূর্ণ। এই অধ্যায়ে আমরা শিখবো `help()`, `dir()` ইত্যাদি টুলস, best practices ও কোড বাগ খুঁজে বের করার পদ্ধতি।

---

## 🧰 1. `help()`, `dir()`, `globals()`, `locals()`

### ✅ কি?

Python-এ কোড বুঝতে ও ব্যবহার জানতে built-in অনেক সহায়ক ফাংশন আছে।

| Function    | কি করে                                 | কোথায় ব্যবহার হয়                            |
| ----------- | -------------------------------------- | ------------------------------------------- |
| `help()`    | object বা ফাংশনের ডকুমেন্টেশন দেখায়    | কোন module বা function কিভাবে কাজ করে বুঝতে |
| `dir()`     | object-এর সব attributes/মেথড দেখায়     | কি কি ফিচার বা method আছে দেখতে             |
| `globals()` | গ্লোবাল স্কোপে থাকা সব ভেরিয়েবল দেখায় | স্কোপে কি কি ভেরিয়েবল আছে দেখতে            |
| `locals()`  | লোকাল স্কোপে থাকা ভেরিয়েবল দেখায়      | ফাংশনের ভেতরে ভেরিয়েবল দেখতে               |

### 🧪 উদাহরণ:

```python
print(help(str))         # str class এর ডকুমেন্টেশন
print(dir(list))         # list এর সব মেথড
print(globals())         # global scope dictionary
print(locals())          # local scope dictionary
```

---

## 📏 2. PEP 8 – Python Code Style Guide

### ✅ কি?

**PEP 8** হলো Python-এর জন্য অফিসিয়াল **কোড স্টাইল গাইডলাইন** — কোন কনভেনশন মেনে কোড লেখা উচিত তা নির্ধারণ করে।

### ✅ কেন?

* কোড হয় **clean, readable এবং maintainable**
* একাধিক ডেভেলপার একসাথে কাজ করতে পারে
* কোডের মান (quality) বজায় থাকে

### ✅ কোথায় ব্যবহার হয়?

* পেশাদার কোডিং প্রকল্পে
* GitHub প্রজেক্ট, Django, Flask প্রজেক্টে
* কোড রিভিউ ও Team Collaboration-এ

### 🔹 কিছু মূল নিয়ম:

| নিয়ম                           | উদাহরণ                      |
| ------------------------------ | --------------------------- |
| ৪টি space ব্যবহার করো (tab নয়) | `def my_function():`        |
| ফাংশন/ভেরিয়েবল নাম ছোট হরফে   | `total_price`, `get_name()` |
| ক্লাস নাম CamelCase            | `class StudentInfo:`        |
| ফাঁকা লাইন রাখো ফাংশনের মাঝে   | `\n` দিয়ে আলাদা করো         |

---

## 🏷 3. Python Naming Conventions

### ✅ কি?

Python-এ কিছু নামকরণ (naming) নিয়ম আছে যা clean ও readable কোড লেখায় সাহায্য করে।

| ধরন          | কনভেনশন            | উদাহরণ                        |
| ------------ | ------------------ | ----------------------------- |
| Variable     | snake\_case        | `user_name`, `total_sum`      |
| Function     | snake\_case        | `get_age()`, `calculate()`    |
| Constant     | UPPER\_CASE        | `PI = 3.14`, `MAX_SIZE = 100` |
| Class        | PascalCase         | `StudentInfo`, `OrderList`    |
| Private Name | \_underscorePrefix | `_secret`, `__hidden`         |

➡️ Code Clean রাখার জন্য এগুলো অনুসরণ করাই ভালো অভ্যাস।

---

## 🐞 4. Common Errors & Debugging Tips

### ✅ কি?

Python-এ অনেক সাধারণ ভুল হয়, যেমন:

* টাইপ ভুল (`TypeError`)
* ভ্যারিয়েবল না পাওয়া (`NameError`)
* index ভুল হওয়া (`IndexError`)
* ফাংশন call ভুল (`AttributeError`)

### ✅ কেন?

* ভুল সমাধান করলে প্রোগ্রাম ভেঙে পড়ে না
* সমস্যা চিহ্নিত করে ঠিক করতে পারি

### ✅ কোথায় ব্যবহার হয়?

* কোডে বাগ খুঁজে বের করতে
* Error Message পড়ে নির্ণয় করতে

### 🧪 উদাহরণ:

```python
a = [1, 2, 3]
print(a[3])  # IndexError: list index out of range

name = "Alice"
print(name.lowercase())  # AttributeError: 'str' object has no attribute 'lowercase'
```

### 🧩 Debugging Tips:

* `print()` দিয়ে variable এর মান দেখো
* `type()` দিয়ে টাইপ চেক করো
* `try-except` ব্লক দিয়ে error ধরো

---

## 🧠 5. Interactive Debugging with `pdb`

### ✅ কি?

`pdb` হলো Python-এর **built-in ডিবাগার**। এটি দিয়ে লাইনে লাইনে কোড এক্সিকিউট করে বাগ খুঁজে বের করা যায়।

### ✅ কেন?

* runtime-এ variable inspect করা যায়
* breakpoint দিয়ে execution থামানো যায়

### ✅ কোথায় ব্যবহার হয়?

* কোন লাইনে কী সমস্যা হচ্ছে তা live দেখে ঠিক করতে
* বড় স্ক্রিপ্ট ডিবাগ করতে

### 🧪 ব্যবহার:

```python
import pdb

def divide(x, y):
    pdb.set_trace()
    return x / y

print(divide(10, 0))  # ZeroDivisionError
```

### 🔹 সাধারণ কমান্ড:

| কমান্ড  | কাজ                          |
| ------- | ---------------------------- |
| `n`     | পরবর্তী লাইনে যায়            |
| `c`     | continue করে স্ক্রিপ্ট চালায় |
| `q`     | quit করে                     |
| `p var` | ভেরিয়েবলের মান প্রিন্ট করে  |

---

## 🧪 Practice Exercises

1. `help(str)` ও `dir(list)` ব্যবহার করে ইনফরমেশন বের করো।
2. একটি ভুল কোডে `try-except` ব্লক দিয়ে সমস্যা ধরো।
3. একটি কোডে `pdb.set_trace()` দিয়ে লাইভ ডিবাগ করো।
4. একটি স্ক্রিপ্ট PEP 8 অনুসারে ঠিক করো (indentation, naming ইত্যাদি)।
5. `globals()` ও `locals()` ব্যবহার করে ভেরিয়েবল চেক করো।

---

## 🧠 Summary

| বিষয়                    | কি?                            | কেন?                                | কোথায় ব্যবহার হয়?                      |
| ----------------------- | ------------------------------ | ----------------------------------- | -------------------------------------- |
| `help()`, `dir()`       | Object info ও methods জানতে    | Documentation ও exploration এর জন্য | নতুন মডিউল বা ফাংশন বুঝতে              |
| `globals()`, `locals()` | স্কোপের ভেরিয়েবল দেখতে        | Debugging ও স্কোপ বোঝার জন্য        | Function বা Module এর মধ্যে            |
| `PEP 8`                 | কোড স্টাইল গাইড                | Readability ও মান বজায় রাখতে        | যে কোন Python প্রজেক্টে                |
| Naming Rules            | ভেরিয়েবল ও ফাংশনের নামের নিয়ম | Convention ও clarity বাড়াতে         | Production, open-source, team projects |
| `pdb`                   | লাইভ ডিবাগিং টুল               | রিয়েল টাইমে সমস্যা খুঁজতে           | Complex বা buggy কোড                   |
