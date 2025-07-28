
# 📘 Lesson 16: JSON, CSV, and File Formats

প্রোগ্রামিংয়ে **স্ট্রাকচার্ড ডেটা** সংরক্ষণ ও আদান-প্রদানের জন্য **JSON** ও **CSV** সবচেয়ে বেশি ব্যবহৃত ফাইল ফরম্যাট। Python-এর মাধ্যমে এই ফাইলগুলো পড়া ও লেখা শেখা গুরুত্বপূর্ণ।

---

## 📦 1. Working with JSON Files

### ✅ কি?

**JSON (JavaScript Object Notation)** হলো একটি human-readable এবং machine-readable ডেটা ফরম্যাট।

### ✅ কেন?

* API, ওয়েব সার্ভিস ও অ্যাপের মধ্যে ডেটা আদান-প্রদানে ব্যবহার হয়।
* Dictionary-র মতো key-value ডেটা সহজে সংরক্ষণ ও পড়া যায়।

### ✅ কোথায় ব্যবহার হয়?

* Web API response save করতে
* অ্যাপের configuration বা settings ফাইলে
* User preferences বা ডেটা স্টোরে

### 📚 Python-এ JSON পড়া ও লেখা:

```python
import json

# Dictionary → JSON file
data = {"name": "Alice", "age": 25}
with open("data.json", "w") as f:
    json.dump(data, f)

# JSON file → Dictionary
with open("data.json", "r") as f:
    loaded_data = json.load(f)
    print(loaded_data["name"])  # Alice
```

---

## 📑 2. Working with CSV Files (csv module)

### ✅ কি?

**CSV (Comma-Separated Values)** হলো টেক্সট ফরম্যাট যেটি টেবুলার ডেটা লাইনে লাইনে সংরক্ষণ করে, যেখানে প্রতিটি কলাম কমা দিয়ে আলাদা করা হয়।

### ✅ কেন?

* এক্সেল বা ডেটাবেজ সফটওয়্যারের সাথে ডেটা আদান-প্রদানে সহজ
* কম জটিলতা ও হালকা ফাইল ফরম্যাট

### ✅ কোথায় ব্যবহার হয়?

* এক্সেল থেকে ডেটা এক্সপোর্ট/ইমপোর্ট করতে
* রিপোর্ট বা লগ জেনারেশন
* ইউজার ডেটা এনালাইসিস

### 📚 Python-এ CSV পড়া ও লেখা:

```python
import csv

# Write CSV
with open("students.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["Name", "Age"])
    writer.writerow(["Mahfuz", 23])
    writer.writerow(["Sara", 21])

# Read CSV
with open("students.csv", "r") as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
```

---

## 🧩 3. Reading and Writing Structured Data

### ✅ কি?

Structured data বলতে বোঝায় এমন ডেটা যেটি **rows & columns**, **key-value pairs**, বা **nested hierarchy** আকারে থাকে।

### ✅ কেন?

* সহজেই ডেটা query, parse ও visualize করা যায়।
* Data analysis, ML, reporting-এর জন্য গুরুত্বপূর্ণ।

### ✅ কোথায় ব্যবহার হয়?

* ডেটাবেজ থেকে ডেটা ফেচ করে সংরক্ষণের সময়
* API থেকে পাওয়া ডেটা ফাইল আকারে সংরক্ষণে
* ডেটা পাইপলাইন ও প্রক্রিয়াকরণে

### 🔧 উদাহরণ: JSON → Python dict → CSV

```python
import json, csv

# Read JSON
with open("data.json") as f:
    data = json.load(f)

# Write to CSV
with open("data.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(data.keys())
    writer.writerow(data.values())
```

---

## 🧪 Practice Exercises

1. একটি Dictionary নাও এবং তা JSON ফাইলে লিখো ও পড়ে দেখাও।
2. একটি CSV ফাইল তৈরি করো যেখানে "Name", "Score" থাকবে।
3. একটি JSON ফাইল থেকে ডেটা পড়ে তা একটি CSV ফাইলে রূপান্তর করো।
4. একটি CSV ফাইল থেকে line-by-line পড়ে স্কোর ৫০ এর বেশি এমন নামগুলো প্রিন্ট করো।

---

## 🧠 Summary

| Format          | কি?                  | কেন ব্যবহার হয়?                          | কোথায় ব্যবহার হয়?                      |
| --------------- | -------------------- | ---------------------------------------- | -------------------------------------- |
| JSON            | Key-value data       | Human + machine readable, nested support | Web API, Config file                   |
| CSV             | টেবুলার ডেটা         | Lightweight, Excel-compatible            | Reports, Excel, Data Exchange          |
| Structured Data | Row/Col বা Key-value | Analysis, Transformation                 | ML, Reporting, File-to-File Conversion |

---
