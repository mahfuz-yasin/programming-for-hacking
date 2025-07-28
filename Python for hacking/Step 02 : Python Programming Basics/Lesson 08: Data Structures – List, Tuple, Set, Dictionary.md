
# 📘 Lesson 08: Data Structures – List, Tuple, Set, Dictionary

## 📌 কী?
Python-এ **Data Structure** হচ্ছে এমন কিছু container যেগুলোর মাধ্যমে আমরা একাধিক মান (value) সংরক্ষণ ও পরিচালনা করতে পারি। এই অধ্যায়ে আমরা শিখবো:

- List → Ordered & Mutable
- Tuple → Ordered & Immutable
- Set → Unordered & Unique
- Dictionary → Key-value pairs

---

## ❓ কেন ব্যবহার হয়?

- ডেটাকে সাজিয়ে, গুছিয়ে ও প্রক্রিয়া করতে
- বিভিন্ন ধরনের সমস্যার জন্য উপযুক্ত format বেছে নিতে
- কোডকে পরিষ্কার, সংক্ষিপ্ত এবং দ্রুত করতে

---

## 🌍 কোথায় ব্যবহার হয়?

| Structure   | কোথায় ব্যবহার হয়                                                |
|-------------|-----------------------------------------------------------------|
| **List**    | item collection, queue/stack, student list                      |
| **Tuple**   | fixed info: coordinates, constants, DB records (read-only)      |
| **Set**     | unique value storage, fast membership test                      |
| **Dict**    | key-value data: API response, configs, name→score mapping       |

---

## 🔹 1. List and List Methods

### ✅ কী?
- Ordered & Mutable (পরিবর্তনযোগ্য)
- Items এর অবস্থান থাকে (indexed)

```python
fruits = ["apple", "banana", "mango"]
````

### 🔧 কেন?

* বারবার পরিবর্তনের প্রয়োজন হলে List সবচেয়ে উপযুক্ত

### ⚙️ Common Methods:

| Method      | Description                        | Example                     |
| ----------- | ---------------------------------- | --------------------------- |
| `append()`  | শেষে item যোগ করে                  | `fruits.append("orange")`   |
| `insert()`  | নির্দিষ্ট স্থানে item ঢোকায়        | `fruits.insert(1, "grape")` |
| `remove()`  | নির্দিষ্ট item মুছে ফেলে           | `fruits.remove("banana")`   |
| `pop()`     | শেষের (বা index অনুযায়ী) item ফেলে | `fruits.pop()`              |
| `sort()`    | লিস্ট sort করে                     | `fruits.sort()`             |
| `reverse()` | উল্টো করে                          | `fruits.reverse()`          |

---

## 🔸 2. List Comprehension and Nesting

### ✅ কী?

* এক লাইনেই লিস্ট তৈরি বা পরিবর্তনের কৌশল
* দ্রুত, সুন্দর ও Pythonic

```python
squares = [x**2 for x in range(5)]
even = [x for x in range(10) if x % 2 == 0]
```

### 🌍 কোথায় ব্যবহার হয়?

* Data filtering & transformation
* Matrix বা nested structure তৈরি

```python
matrix = [
    [1, 2],
    [3, 4]
]
print(matrix[1][0])  # Output: 3
```

---

## 🔹 3. Tuple and Immutability

### ✅ কী?

* Ordered but Immutable (পরিবর্তন অযোগ্য)

```python
person = ("Alice", 25, "Engineer")
```

### ❓ কেন?

* নিরাপদ ও দ্রুত (safe & fast)
* fixed data store করতে

### 🌍 কোথায় ব্যবহার হয়?

* Coordinates, RGB, DB record (read-only), constants

---

## 🔸 4. Set and Set Operations

### ✅ কী?

* Unordered collection, only unique items
* Fast membership checking

```python
colors = {"red", "green", "blue"}
```

### 🌍 কোথায় ব্যবহার হয়?

* Duplicate বাদ দিয়ে collection store করতে
* Set theory (Union, Intersection) প্রয়োগ করতে

### 🔧 Set Operations:

```python
A = {1, 2, 3}
B = {3, 4, 5}
print(A | B)  # Union
print(A & B)  # Intersection
```

---

## 🔹 5. Dictionary and Dictionary Methods

### ✅ কী?

* Key-value pair storage
* Indexed by key, not by position

```python
student = {
    "name": "Mahfuz",
    "age": 22,
    "course": "Python"
}
```

### 🌍 কোথায় ব্যবহার হয়?

* JSON/API data, database-like storage, configs

### 🛠️ Common Methods:

| Method     | কাজ                          |
| ---------- | ---------------------------- |
| `get()`    | key অনুযায়ী মান ফেরত দেয়     |
| `keys()`   | সব key দেয়                   |
| `values()` | সব value দেয়                 |
| `items()`  | key-value জোড়া দেয়           |
| `update()` | নতুন key-value যোগ/আপডেট করে |
| `pop()`    | নির্দিষ্ট key বাদ দেয়        |

---

## ⚖️ 6. List vs Tuple vs Set vs Dict

| Feature     | List         | Tuple      | Set        | Dictionary            |
| ----------- | ------------ | ---------- | ---------- | --------------------- |
| Syntax      | `[1, 2]`     | `(1, 2)`   | `{1, 2}`   | `{"a": 1}`            |
| Ordered?    | ✅ Yes        | ✅ Yes      | ❌ No       | ❌ No (3.7+ = ordered) |
| Duplicates? | ✅ Allowed    | ✅ Allowed  | ❌ No       | ✅ Allowed (in values) |
| Mutable?    | ✅ Yes        | ❌ No       | ✅ Yes      | ✅ Yes                 |
| Indexed?    | ✅ By index   | ✅ By index | ❌          | ✅ By key              |
| Use Case    | General list | Fixed set  | Unique set | Key → Value mapping   |

---

## 🧭 Practice Exercises

1. লিস্টে item যোগ করে sort করো।
2. টাপল থেকে নির্দিষ্ট index-এর মান বের করো।
3. দুটি সেটের union এবং intersection দেখাও।
4. ডিকশনারিতে নতুন key যোগ করো এবং একটি key মুছে ফেলো।
5. List comprehension দিয়ে ১-২০ পর্যন্ত বর্গসংখ্যা বের করো।

---

## 🧠 Summary

| Structure | কী?                | কেন ব্যবহার হয়                              | কোথায় ব্যবহার হয়                    |
| --------- | ------------------ | ------------------------------------------- | ----------------------------------- |
| List      | Ordered, Mutable   | Sequence store ও edit করার জন্য             | Generic collections, stack, queue   |
| Tuple     | Ordered, Immutable | Constant value, fast access                 | DB records, coordinates, fixed info |
| Set       | Unordered, Unique  | Duplicate remove ও membership test          | Tags, Unique users, Math sets       |
| Dict      | Key-value mapping  | Structure data store ও দ্রুত access এর জন্য | JSON, Configs, User Profile         |
