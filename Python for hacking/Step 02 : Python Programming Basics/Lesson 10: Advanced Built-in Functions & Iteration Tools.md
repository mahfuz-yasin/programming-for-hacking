
# 📘 Lesson 10: Advanced Built-in Functions & Iteration Tools

## 📌 কী?
Python-এর এই ফাংশনগুলো হলো কিছু **উন্নত বিল্ট-ইন ফাংশন** যা ডেটা প্রসেসিং, লুপিং, সোর্টিং, ও কন্ডিশনাল চেক করার কাজ সহজ করে তোলে।

---

## ❓ কেন ব্যবহার হয়?
- কোডকে সংক্ষিপ্ত ও কার্যকরী করতে
- functional programming সুবিধা পেতে
- iteration ও ডেটা হ্যান্ডলিং সহজ করতে
- cleaner, faster, and more Pythonic code লেখার জন্য

---

## 🌍 কোথায় ব্যবহার হয়?
- **ডেটা সায়েন্স ও এনালাইসিসে** large list বা dataset প্রক্রিয়াকরণে
- **ওয়েব ডেভেলপমেন্টে** ডেটা filter, map বা zip করতে
- **ফাইল প্রসেসিং, API response, GUI, automation** ইত্যাদিতে
- **Competitive programming বা Interview coding challenges** এ

---

## 🔁 1. `map()`, `filter()`, `reduce()`

### 🔹 `map(function, iterable)`
#### ➤ কি করে?
একটি ফাংশন লিস্টের প্রতিটি আইটেমে প্রয়োগ করে।

#### ➤ কোথায় ব্যবহার হয়?
- list থেকে transform (e.g., square, upper case)
- data pipeline বা functional chain-এ

```python
nums = [1, 2, 3, 4]
squares = list(map(lambda x: x**2, nums))
print(squares)  # [1, 4, 9, 16]
````

---

### 🔹 `filter(function, iterable)`

#### ➤ কি করে?

শুধু সেই আইটেমগুলো রাখে যেগুলোর জন্য function `True` রিটার্ন করে।

#### ➤ কোথায় ব্যবহার হয়?

* even/odd ফিল্টার করতে
* condition অনুযায়ী dataset ছোট করতে

```python
even = list(filter(lambda x: x % 2 == 0, nums))
print(even)  # [2, 4]
```

---

### 🔹 `reduce(function, iterable)`

#### ➤ কি করে?

একটি ফাংশন দিয়ে পুরো iterable কে single value-তে reduce করে।

#### ➤ কোথায় ব্যবহার হয়?

* যোগফল, গুণফল, সর্বোচ্চ/সর্বনিম্ন বের করতে
* accumulator টাইপ অপারেশনে

```python
from functools import reduce
total = reduce(lambda a, b: a + b, nums)
print(total)  # 10
```

---

## 🔃 2. `sorted()`, `reversed()`, `any()`, `all()`

### 🔹 `sorted()`

#### ➤ কি করে?

লিস্ট বা iterable sort করে দেয় (default: ascending)।

#### ➤ কোথায় ব্যবহার হয়?

* ডেটা visualization বা রিপোর্টে সাজিয়ে দেখাতে
* Ranking বা ordering করতে

```python
names = ["Zara", "Ali", "Bob"]
print(sorted(names))  # ['Ali', 'Bob', 'Zara']
```

---

### 🔹 `reversed()`

#### ➤ কি করে?

একটি iterable কে উল্টো করে।

#### ➤ কোথায় ব্যবহার হয়?

* লাস্ট ইনফর্মেশন আগে দেখাতে
* reverse traversal করতে

```python
rev = list(reversed(names))  # ['Bob', 'Ali', 'Zara']
```

---

### 🔹 `any()`

#### ➤ কি করে?

একটি iterable-এ যদি **একটি True** পাওয়া যায় তাহলে `True` দেয়।

#### ➤ কোথায় ব্যবহার হয়?

* কমপক্ষে একটি শর্ত match করছে কিনা জানার জন্য

```python
values = [0, 0, 1]
print(any(values))  # True
```

---

### 🔹 `all()`

#### ➤ কি করে?

সবগুলো value যদি `True` হয় তাহলে `True` দেয়।

#### ➤ কোথায় ব্যবহার হয়?

* নিশ্চিত করতে সব শর্ত পূরণ হয়েছে কিনা

```python
flags = [True, True, False]
print(all(flags))  # False
```

---

## 🔗 3. `zip()`, `enumerate()`, `len()`, `sum()`

### 🔸 `zip()`

#### ➤ কি করে?

একাধিক iterable-এর আইটেমগুলো pair করে দেয়।

#### ➤ কোথায় ব্যবহার হয়?

* দুটি লিস্ট যুক্ত করে রিপোর্ট বা টেবিল তৈরি করতে

```python
names = ["A", "B"]
scores = [90, 85]
for n, s in zip(names, scores):
    print(f"{n}: {s}")
```

---

### 🔸 `enumerate()`

#### ➤ কি করে?

লিস্টের সাথে index-number সহ tuple তৈরি করে।

#### ➤ কোথায় ব্যবহার হয়?

* item-এর অবস্থানসহ প্রিন্ট করতে

```python
fruits = ["apple", "banana", "cherry"]
for i, fruit in enumerate(fruits):
    print(i, fruit)
```

---

### 🔸 `len()`

#### ➤ কি করে?

একটি iterable-এর দৈর্ঘ্য (item সংখ্যা) বলে।

#### ➤ কোথায় ব্যবহার হয়?

* size check, validation, loop limits

```python
print(len(fruits))  # 3
```

---

### 🔸 `sum()`

#### ➤ কি করে?

iterable-এর সব numeric মান যোগফল বের করে।

#### ➤ কোথায় ব্যবহার হয়?

* total, average, percentage ইত্যাদিতে

```python
nums = [1, 2, 3, 4]
print(sum(nums))  # 10
```

---

## 🧪 Practice Exercises

1. `map()` দিয়ে একটি লিস্টের সব item-এর স্কয়ার বের করো।
2. `filter()` দিয়ে শুধুমাত্র even নাম্বার বের করো।
3. `reduce()` দিয়ে ১ থেকে ১০ পর্যন্ত সংখ্যার গুণফল বের করো।
4. `zip()` দিয়ে দুটি লিস্ট মিলে রিপোর্ট বানাও।
5. `enumerate()` ব্যবহার করে index সহ list দেখাও।
6. `any()` এবং `all()` দিয়ে condition checker বানাও।

---

## 🧠 Summary Table

| Function      | কী করে                        | কোথায় ব্যবহার হয়                           |
| ------------- | ----------------------------- | ------------------------------------------ |
| `map()`       | সব item-এ function apply করে  | list transformation, data cleaning         |
| `filter()`    | True item গুলো রেখে দেয়       | conditional filtering (e.g., even numbers) |
| `reduce()`    | সব item মিলে single value দেয় | যোগফল, গুণফল, cumulative score             |
| `sorted()`    | সাজিয়ে ফেলে                   | reports, rankings, visualization           |
| `reversed()`  | উল্টো করে                     | reverse order, last-to-first               |
| `any()`       | কমপক্ষে ১টি True খুঁজে        | validation, partial match                  |
| `all()`       | সব যদি True, তবে True দেয়     | all conditions met, total validation       |
| `zip()`       | multiple iterable একসাথে চলায় | combine data, generate tables              |
| `enumerate()` | item এর সাথে index দেয়        | indexed printing, debugging                |
| `len()`       | item সংখ্যা বের করে           | input validation, loop range               |
| `sum()`       | total যোগফল দেয়               | aggregate scores, totals                   |
