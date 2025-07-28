
# 📘 Lesson 07: Loops and Loop Control

## 📌 কী?
**Loop** হলো এমন একটি প্রোগ্রামিং কৌশল, যার মাধ্যমে **একটি কোড ব্লক বারবার** চালানো যায় যতক্ষণ না একটি নির্দিষ্ট শর্ত পূরণ হয়। Python-এ মূলত দুটি লুপ রয়েছে — `for` এবং `while`, এবং লুপকে নিয়ন্ত্রণ করার জন্য রয়েছে `break`, `continue`, ও `pass`।

---

## ❓ কেন ব্যবহার হয়?

- পুনরাবৃত্ত কাজ একাধিকবার করাতে
- তালিকা (list), সেট (set), ডিকশনারি (dict) ইত্যাদির উপর লুপ চালাতে
- automation ও iteration সহজ করতে
- unnecessary কোড রেপিটিশন এড়াতে

---

## 🌍 কোথায় ব্যবহার হয়?

| Context          | ব্যবহার                          |
|------------------|----------------------------------|
| Data processing  | list/set/dict-এর উপর লুপ চালিয়ে মান প্রসেস করতে  
| User input loop  | যতক্ষণ না সঠিক ইনপুট পাওয়া যায়  
| Searching/filtering | নির্দিষ্ট মান খুঁজতে বা বাদ দিতে  
| Game/GUI/Backend | condition-based repeat action নিতে  
| File handling    | ফাইলের প্রতিটি লাইন বা item পড়তে  

---

## 🔁 1. `for` Loop

### ✅ কী করে?
- iterable (list, string, range) এর প্রতিটি element এর উপর লুপ চালায়

### 🧪 Syntax:
```python
for variable in iterable:
    # loop body
````

### 🎯 উদাহরণ:

```python
for i in range(5):
    print("Number:", i)

fruits = ["apple", "banana", "mango"]
for fruit in fruits:
    print(fruit)
```

---

## 🔄 2. `while` Loop

### ✅ কী করে?

* যতক্ষণ নির্দিষ্ট condition `True` থাকবে, ততক্ষণ চলতে থাকবে

### 🧪 Syntax:

```python
while condition:
    # loop body
```

### 🎯 Example:

```python
x = 1
while x <= 5:
    print(x)
    x += 1
```

⚠️ ভুল condition দিলে infinite loop হতে পারে।

---

## ⛔ 3. Loop Control: `break`, `continue`, `pass`

### 🔹 `break` – লুপ একেবারে থামিয়ে দেয়

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

### 🔹 `continue` – current iteration স্কিপ করে পরেরটিতে চলে যায়

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

### 🔹 `pass` – কোনো কাজ করে না, future logic placeholder

```python
for i in range(3):
    pass  # Later logic will be added
```

---

## 🔂 4. `else` with Loops

### ✅ কী করে?

* যদি loop স্বাভাবিকভাবে শেষ হয় (without `break`), তাহলে `else` ব্লক চালায়

### 🎯 Example:

```python
for i in range(5):
    print(i)
else:
    print("Loop ended without break.")
```

### ⚠️ `break` থাকলে `else` চালানো হয় না:

```python
for i in range(5):
    if i == 3:
        break
    print(i)
else:
    print("This won't print.")
```

---

## 📦 5. `range()`, `enumerate()`, `zip()`

### 🔸 `range(start, stop, step)`

* সংখ্যা জেনারেট করতে

```python
for i in range(1, 10, 2):  # 1, 3, 5, 7, 9
    print(i)
```

---

### 🔸 `enumerate(iterable)`

* index সহ item দেয় (tuple আকারে)

```python
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(index, fruit)
```

---

### 🔸 `zip(iterable1, iterable2)`

* দুটি iterable কে pair করে দেয়

```python
names = ["Alice", "Bob"]
scores = [85, 90]

for name, score in zip(names, scores):
    print(f"{name} scored {score}")
```

---

## 🧭 Practice Exercises

1. `for` loop দিয়ে ১ থেকে ১০ পর্যন্ত সংখ্যার যোগফল বের করো।
2. `continue` দিয়ে ১ থেকে ৫ এর মধ্যে শুধু odd সংখ্যা প্রিন্ট করো।
3. `while` loop দিয়ে ইউজার যতক্ষণ না "exit" লেখে, ইনপুট নিতে থাকো।
4. `enumerate()` দিয়ে একটি list-এর index ও মান দেখাও।
5. `zip()` দিয়ে দুটি list-এর তথ্য একত্রে `Name:Score` ফরম্যাটে দেখাও।

---

## 🧠 Summary

| ফিচার         | কী করে                                      | কোথায় ব্যবহার হয়                    |
| ------------- | ------------------------------------------- | ----------------------------------- |
| `for` loop    | iterable item এর উপর লুপ চালায়              | list, string, range ইত্যাদির উপর    |
| `while` loop  | condition true থাকলে লুপ চালায়              | user input, menu, repeat until done |
| `break`       | লুপ সম্পূর্ণভাবে থামিয়ে দেয়                 | error detection, early exit         |
| `continue`    | current iteration স্কিপ করে পরেরটিতে যায়    | skip unwanted case, filtering       |
| `pass`        | ফাঁকা ব্লক, placeholder                     | future logic add করতে               |
| `else`        | loop শেষে নির্দিষ্ট কাজ করায় (break না হলে) | loop success feedback দিতে          |
| `range()`     | সংখ্যার সিরিজ তৈরি করে                      | for loop iteration                  |
| `enumerate()` | index সহ item দেয়                           | indexed loop/control                |
| `zip()`       | একাধিক iterable কে pair করে                 | combine two lists                   |
