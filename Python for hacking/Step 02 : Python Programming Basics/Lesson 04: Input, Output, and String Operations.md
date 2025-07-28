
# 📘 Lesson 04: Input, Output, and String Operations

## 📌 কি?
এই অধ্যায়ে শিখবো কিভাবে Python-এ:
- ইউজারের কাছ থেকে ডেটা ইনপুট নিতে হয় (`input()`)
- স্ক্রিনে ফলাফল বা তথ্য প্রিন্ট করতে হয় (`print()`)
- স্ট্রিং-এর উপর কাজ করতে হয় (indexing, slicing, methods)

---

## ❓ কেন ব্যবহার হয়?
- ইউজারের কাছ থেকে ডেটা নিতে (ইনপুট)
- প্রোগ্রামের ফলাফল বা বার্তা দেখাতে (আউটপুট)
- টেক্সট বা বাক্যকে প্রক্রিয়া করতে (স্ট্রিং ম্যানিপুলেশন)
- ফর্ম, প্রশ্নোত্তর, ফাইল-নেম, ইউজারনেম প্রসেস করতে

---

## 🌍 কোথায় ব্যবহার হয়?
| ফিচার         | ব্যবহার ক্ষেত্র                            |
|---------------|--------------------------------------------|
| `input()`     | ফর্ম ফিলাপ, প্রশ্ন-উত্তর, ইউজার কমান্ড     |
| `print()`     | ফলাফল দেখানো, ডিবাগ, লগ মেসেজ              |
| String ops    | টেক্সট প্রসেসিং, ইউজারনেম যাচাই, ফাইল নেম |

---

## 🧾 1. Input and Output in Python

### 🔹 `input()` – ইউজার থেকে ইনপুট:

```python
name = input("Enter your name: ")
print("Hello,", name)
````

📌 সব ইনপুট `string` টাইপে আসে
📌 সংখ্যা পেতে `int()` বা `float()` কনভার্ট দরকার

```python
age = int(input("Enter age: "))
print("Next year you’ll be", age + 1)
```

---

### 🔹 `print()` – আউটপুট দেখানো:

```python
print("Sum =", 5 + 3)
print("Name", "Age", sep=" | ", end=" DONE\n")
```

| Parameter | কাজ                                  |
| --------- | ------------------------------------ |
| `sep`     | একাধিক আইটেমের মাঝে যা বসবে          |
| `end`     | লাইনের শেষে কী থাকবে (default: `\n`) |

---

## 🧵 2. String Indexing & Slicing

### 🔹 Indexing:

```python
text = "Python"
print(text[0])   # P
print(text[-1])  # n
```

### 🔹 Slicing:

```python
text = "Programming"
print(text[0:4])  # Prog
print(text[3:])   # gramming
print(text[:5])   # Progr
```

### 🔹 Step Slicing:

```python
print(text[::2])  # Pormig
```

📌 **কোথায় ব্যবহার হয়?** → অংশবিশেষ বের করতে, substring তুলনা করতে, টেক্সট ট্রিম করতে

---

## 🧰 3. f-strings and format()

### 🔹 f-string:

```python
name = "Alice"
age = 25
print(f"My name is {name} and I am {age} years old.")
```

### 🔹 `format()`:

```python
print("My name is {} and I am {}".format(name, age))
```

📌 **কেন দরকার?** → ডেটা সহ স্ট্রিং সহজে তৈরি করতে
📌 **কোথায়?** → রিপোর্ট, UI টেক্সট, লগ ফরম্যাটিং

---

## 🧩 4. String Methods: `join()`, `split()`, `replace()`

| Method      | কাজ                            | উদাহরণ                              |
| ----------- | ------------------------------ | ----------------------------------- |
| `join()`    | লিস্ট → স্ট্রিং                | `" ".join(["Python", "is", "fun"])` |
| `split()`   | স্ট্রিং → লিস্ট                | `"a-b-c".split("-")`                |
| `replace()` | নির্দিষ্ট অংশ অন্য দিয়ে বদলানো | `"hello".replace("l", "x")`         |

### উদাহরণ:

```python
text = "I love Python"
words = text.split()           # ['I', 'love', 'Python']
joined = "-".join(words)       # I-love-Python
new_text = text.replace("love", "use")  # I use Python
```

📌 **কোথায়?** → সার্চ, ফাইলনেম ঠিক করা, ইউজার ইনপুট কাস্টমাইজ করা

---

## 🔍 5. String Comparison and Manipulation

### 🔹 Comparison:

```python
print("apple" == "Apple")   # False
print("abc" < "abd")        # True
```

### 🔹 Useful Methods:

| Method         | ব্যাখ্যা                          |
| -------------- | --------------------------------- |
| `lower()`      | সব ছোট হরফে রূপান্তর              |
| `upper()`      | সব বড় হরফে রূপান্তর               |
| `capitalize()` | প্রথম অক্ষর বড় করে                |
| `startswith()` | শুরুতে নির্দিষ্ট শব্দ আছে কিনা    |
| `endswith()`   | শেষে নির্দিষ্ট শব্দ আছে কিনা      |
| `strip()`      | শুরু ও শেষে ফাঁকা জায়গা মুছে ফেলে |

```python
s = "  Hello World!  "
print(s.strip())           # "Hello World!"
print("python".startswith("py"))  # True
```

📌 **কোথায়?** → ইনপুট যাচাই, ফাইল বা ইউজারনেম চেক, ফরম্যাট ঠিক করা

---

## 🧪 Practice Exercises

1. ইউজারের নাম ও বয়স ইনপুট নিয়ে প্রিন্ট করো:

```
Hello, Mahfuz. You are 25 years old.
```

2. একটি স্ট্রিং নাও এবং প্রথম ৫ অক্ষর প্রিন্ট করো।

3. একটি স্ট্রিং-এর সব `a` → `@` দিয়ে replace করো।

4. একটি বাক্য split করে word-wise প্রিন্ট করো।

---

## 🧠 Summary

| টপিক             | ব্যাখ্যা                                            |
| ---------------- | --------------------------------------------------- |
| `input()`        | ইউজার থেকে string ইনপুট নেয়                         |
| `print()`        | স্ক্রিনে তথ্য দেখায়; `sep`, `end` দিয়ে কাস্টমাইজ    |
| Indexing/Slicing | স্ট্রিং-এর অংশ বের করতে সাহায্য করে                 |
| f-string/format  | ডেটা সহ সহজে স্ট্রিং তৈরি                           |
| String Methods   | `split()`, `join()`, `replace()`, `strip()` ইত্যাদি |
