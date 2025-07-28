
# 📘 Lesson 11: Exception Handling

## 📌 কী?  
**Exception Handling** হলো প্রোগ্রামের এমন একটি কৌশল যা কোনো **Error (ত্রুটি)** ঘটলে প্রোগ্রামকে হঠাৎ থামিয়ে না দিয়ে, **পরিকল্পিতভাবে পরিচালনা** করে। Python-এ `try`, `except`, `else`, `finally` দিয়ে এটি করা হয়।

---

## ❓ কেন ব্যবহার হয়?

- প্রোগ্রামকে **crash হওয়া থেকে রক্ষা** করতে।
- ইউজারকে **উপযোগী বার্তা** দেখাতে।
- **কনট্রোলড ফ্লো** বজায় রাখতে।
- বড় অ্যাপ্লিকেশনে **debug ও logging** সুবিধা দিতে।

---

## 🌍 কোথায় ব্যবহার হয়?

- ফাইল খোলা (file not found)
- ইউজার ইনপুট (ভুল টাইপ)
- নেটওয়ার্ক রিকোয়েস্ট
- ডাটাবেজ কানেকশন
- ওয়েব API ব্যবহার
- যেকোনো runtime error এর সময়

---

## 🔹 1. `try`, `except`, `else`, `finally`

### ✅ Syntax:
```python
try:
    # কোড যা Error দিতে পারে
except SomeError:
    # Error হলে যা হবে
else:
    # Error না হলে যা হবে
finally:
    # যাই হোক এটা হবেই
````

### 🧪 উদাহরণ:

```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ZeroDivisionError:
    print("Cannot divide by zero.")
except ValueError:
    print("Invalid input. Please enter a number.")
else:
    print("Result is:", result)
finally:
    print("Execution completed.")
```

### 🧠 ব্যাখ্যা:

| ব্লক      | কাজ                                       |
| --------- | ----------------------------------------- |
| `try`     | সন্দেহজনক কোড (যেখানে exception হতে পারে) |
| `except`  | error হলে এখানে আসে                       |
| `else`    | error না হলে এই ব্লক চলে                  |
| `finally` | সবশেষে সব অবস্থায় এই ব্লক চলবেই           |

---

## 🔸 2. Multiple Exceptions

একাধিক সম্ভাব্য exception আলাদা করে handle করা যায়।

```python
try:
    x = int(input("Enter a number: "))
    print(10 / x)
except ValueError:
    print("Enter a valid number.")
except ZeroDivisionError:
    print("You can't divide by 0.")
except Exception as e:
    print("Unexpected error:", e)
```

✅ ভালো প্র্যাকটিস: সাধারণ Exception ধরার আগে নির্দিষ্ট Exception ধরো।

---

## 🚨 3. Raising Custom Exceptions

### 🔹 কী?

নিজের মতো করে exception তৈরি করা, যাতে কোনো বিশেষ পরিস্থিতিতে নিজেই error trigger করা যায়।

### ✅ Syntax:

```python
raise ExceptionType("Custom error message")
```

### 🧪 Example:

```python
def check_age(age):
    if age < 0:
        raise ValueError("Age cannot be negative")
    print("Valid age")

check_age(25)       # Valid
check_age(-5)       # Raises ValueError
```

### ➕ Custom Exception Class:

```python
class MyError(Exception):
    pass

raise MyError("This is a custom error.")
```

---

## 🧭 Practice Exercises

1. `try-except` ব্যবহার করে ইউজারের দেওয়া সংখ্যার square বের করো।
2. `ZeroDivisionError` ও `ValueError` আলাদাভাবে handle করো।
3. একটি ফাংশন লেখো যা নেগেটিভ বয়স ইনপুট পেলে Custom Exception ছুঁড়ে দেয়।
4. `finally` ব্লকে “Thank you!” প্রিন্ট করো।

---

## 🧠 Summary

| টপিক             | উদ্দেশ্য                                          |
| ---------------- | ------------------------------------------------- |
| `try`            | সন্দেহজনক কোড যেখানে exception ঘটতে পারে          |
| `except`         | exception ধরার জন্য                               |
| `else`           | যদি কোনো exception না ঘটে, তখন এই কোড চলে         |
| `finally`        | সবশেষে সবসময় চালানো হয়                            |
| `raise`          | নিজে থেকে exception ছুঁড়ে দেওয়া                   |
| Custom Exception | নিজের error message বা class define করে raise করা |

---