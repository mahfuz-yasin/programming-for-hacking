
# 📘 Lesson 09: Functions and Lambda

## 📌 কী?
**Function** হলো কোডের এমন একটি অংশ, যা বারবার ব্যবহার করা যায়।  
**Lambda function** হলো ছোট আকারের এক-লাইনের unnamed function।

---

## ❓ কেন ব্যবহার হয়?
- কোড **reusable ও modular** করতে
- **ক্লিন, সংক্ষিপ্ত ও maintainable** কোড লিখতে
- বড় সমস্যা ছোট ছোট অংশে ভাগ করে সমাধান করতে
- Functional programming-এর সুবিধা পেতে

---

## 🌍 কোথায় ব্যবহার হয়?
- ওয়েব অ্যাপ্লিকেশনে ইউজার ইনপুট প্রক্রিয়াকরণে
- API/Modules-এর কোড স্ট্রাকচারে
- **Data Science** ও **Machine Learning**-এ data transform/filter করতে
- Python automation, GUI ও backend logic তৈরিতে

---

## 🔹 1. Function Declaration and Calling

### ✅ Syntax:
```python
def function_name(parameters):
    # function body
    return result
````

### 🧪 উদাহরণ:

```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Mahfuz"))  # Hello, Mahfuz!
```

🔍 **কেন?**

* কাজকে বারবার না লিখে পুনঃব্যবহার করা যায়।

---

## 🔸 2. Function Arguments: Positional, Keyword, Default

### ➤ Positional:

```python
def add(a, b):
    return a + b

print(add(2, 3))  # 5
```

### ➤ Keyword:

```python
print(add(b=3, a=2))  # 5
```

### ➤ Default:

```python
def greet(name="Guest"):
    return f"Hello, {name}!"
```

🔍 **কেন?**

* ফাংশনের প্যারামিটার নিয়ন্ত্রণ সহজ হয়।

---

## ✳️ 3. `*args` and `**kwargs`

### ➤ `*args` = একাধিক unnamed argument (tuple):

```python
def add_all(*args):
    return sum(args)

print(add_all(1, 2, 3))  # 6
```

### ➤ `**kwargs` = একাধিক named argument (dict):

```python
def show(**kwargs):
    for k, v in kwargs.items():
        print(f"{k}: {v}")
```

🔍 **কেন?**

* dynamic number of arguments handle করার জন্য।

---

## 🪄 4. Lambda Functions (Anonymous Functions)

### ✅ Syntax:

```python
lambda arguments: expression
```

### 🧪 উদাহরণ:

```python
square = lambda x: x ** 2
print(square(4))  # 16
```

### ➤ Real Use:

```python
nums = [1, 2, 3]
print(list(map(lambda x: x*2, nums)))  # [2, 4, 6]
```

🔍 **কেন?**

* Simple ও দ্রুত ব্যবহারযোগ্য function লিখতে।

🌍 **কোথায়?**

* `map()`, `filter()`, GUI callback, event-driven প্রোগ্রামিংয়ে।

---

## 🌐 5. Scope and Global vs Local

### 🔸 Local Scope:

```python
def my_func():
    x = 10  # local
    print(x)
```

### 🔸 Global Scope:

```python
x = 5

def show():
    print(x)  # global x
```

### 🔸 Modify Global:

```python
count = 0
def inc():
    global count
    count += 1
```

🔍 **কেন?**

* ভিন্ন ভিন্ন অংশে একে অপরের পরিবর্তন ঠেকাতে।

---

## 🔁 6. Recursion (Basic)

### 🔹 কী?

একটি ফাংশন যখন নিজেকেই কল করে।

### 🧪 Example:

```python
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)
```

🔍 **কেন?**

* সমস্যাকে ছোট ছোট অংশে ভাগ করে সমাধান করতে।

🌍 **কোথায়?**

* গাণিতিক সমাধান, ট্রী ট্রাভার্সাল, ব্যাকট্র্যাকিং, ডেটা স্ট্রাকচারে।

---

## 🧪 Practice Exercises

1. ফাংশনে ৩টি সংখ্যার গড় বের করো।
2. lambda দিয়ে even checker বানাও।
3. `*args` দিয়ে যোগফল বের করো।
4. `**kwargs` দিয়ে profile প্রিন্ট করো।
5. Recursion দিয়ে n তম Fibonacci বের করো।

---

## 🧠 Summary

| টপিক            | কী করে                     | কোথায় ব্যবহার হয়                |
| --------------- | -------------------------- | ------------------------------- |
| `def`           | ফাংশন তৈরি করে             | Reusable logic                  |
| `return`        | ফাংশনের আউটপুট ফেরত দেয়    | Value calculations              |
| Positional args | position অনুযায়ী মান নেয়   | General usage                   |
| Keyword args    | নাম দিয়ে মান পাস করে       | Code readability                |
| Default args    | default value সেট করা থাকে | Optional values                 |
| `*args`         | একাধিক unnamed মান নেয়     | Calculator, aggregator          |
| `**kwargs`      | একাধিক named মান নেয়       | Dynamic data printing           |
| Lambda          | ছোট একলাইন ফাংশন           | map, filter, sort               |
| Scope           | কোন ভেরিয়েবল কোথায় active | Bug fixing, variable visibility |
| Recursion       | ফাংশন নিজেকে কল করে        | Trees, mathematical series      |
