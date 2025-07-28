
# 📘 Lesson 06: Control Flow – If Else and Conditions

## 📌 কী?
**Control Flow** হলো প্রোগ্রামের এমন একটি কাঠামো, যা সিদ্ধান্ত নেয় কোন অংশের কোড চালানো হবে।  
Python-এ এটি করা হয় `if`, `elif`, `else` স্টেটমেন্ট এবং condition expression-এর মাধ্যমে।

---

## ❓ কেন ব্যবহার হয়?
- Decision making বাস্তব জীবনের মতোই প্রোগ্রামে প্রয়োগ করতে
- একাধিক শর্ত অনুযায়ী ভিন্ন আউটপুট বা কাজ করতে
- কোডের লজিক অনুযায়ী branching তৈরি করতে

---

## 🌍 কোথায় ব্যবহার হয়?
| Context            | ব্যবহার                                         |
|--------------------|--------------------------------------------------|
| বয়স যাচাই          | `if age >= 18: print("Adult")`                 |
| ফলাফল নির্ধারণ     | Pass/Fail স্ট্যাটাস বের করতে                    |
| লগিন যাচাই         | ইউজারনেম/পাসওয়ার্ড মিললে ঢুকতে দেওয়া          |
| ওয়েব অ্যাপ লজিক     | ভিন্ন রুটে redirect করার সময়                  |
| Test/Validation    | শর্ত অনুযায়ী ইনপুট যাচাই ও বার্তা দেখাতে       |

---

## 🔹 1. Conditional Statements: `if`, `elif`, `else`

### ✅ Syntax:
```python
if condition:
    # block if condition is True
elif another_condition:
    # block if elif is True
else:
    # block if all above are False
````

### 🧪 Example:

```python
age = 18

if age >= 18:
    print("You are an adult.")
elif age >= 13:
    print("You are a teenager.")
else:
    print("You are a child.")
```

📌 **কি?** → নির্দিষ্ট শর্ত অনুযায়ী কোড চালানো
🎯 **কেন?** → ডাইনামিক decision নেওয়ার জন্য
🧩 **কোথায়?** → ফর্ম validation, বয়স ভিত্তিক decision ইত্যাদিতে

---

## 🔸 2. Boolean Expressions and Short Circuiting

### ✅ Operators:

* তুলনা: `==`, `!=`, `>`, `<`, `>=`, `<=`
* লজিক: `and`, `or`, `not`

### 🔄 Short Circuiting:

* `and`: প্রথম False পেলেই বাকিটা চেক করে না
* `or`: প্রথম True পেলেই বাকিটা চেক করে না

### 🧪 Example:

```python
def check():
    print("Checking...")
    return True

print(False and check())   # check() won't run
print(True or check())     # check() won't run
```

🎯 **কেন?** → Efficiency বাড়ানোর জন্য
🧩 **কোথায়?** → শর্ত অনেক হলে unnecessary check এড়াতে

---

## ⚡ 3. Ternary Operator (One-liner If-Else)

### ✅ Syntax:

```python
value = A if condition else B
```

### 🧪 Example:

```python
age = 17
status = "Adult" if age >= 18 else "Minor"
print(status)  # Minor
```

📌 **কি?** → সংক্ষিপ্ত `if-else`
🎯 **কেন?** → কোড ছোট ও readable রাখতে
🧩 **কোথায়?** → status, label বা simple condition এ

---

## 🛑 4. `assert` Statement

### ✅ Syntax:

```python
assert condition, "Error message"
```

### 🧪 Example:

```python
x = 5
assert x > 0, "x must be positive"
```

📌 **কি?** → এক্সপ্রেশন True না হলে Error দেয়
🎯 **কেন?** → debugging/testing সময় validate করতে
🧩 **কোথায়?** → input validation, test-driven development-এ

---

## 🧭 Practice Exercises

1. ইউজার থেকে বয়স ইনপুট নিয়ে নিচের নিয়মে প্রিন্ট করো:

   * 18 বা বেশি → "Adult"
   * 13-17 → "Teenager"
   * নিচে → "Child"

2. নিচের Ternary operator ব্যবহার করো:

```python
marks = 85
status = "Pass" if marks >= 40 else "Fail"
```

3. assert দিয়ে নিশ্চিত করো ইউজার ইনপুট > 0:

```python
x = int(input("Enter number: "))
assert x > 0, "Number must be greater than zero"
```

---

## 🧠 Summary

| টপিক             | কাজ                                     | ব্যবহার হয়                        |
| ---------------- | --------------------------------------- | --------------------------------- |
| `if`             | শর্ত True হলে ব্লক চালায়                | Decision making                   |
| `elif`           | উপরের শর্ত False হলে চেক করে            | Multiple condition                |
| `else`           | সব শর্ত False হলে fallback block চালায়  | Final fallback decision           |
| Boolean Ops      | `and`, `or`, `not` → multiple condition | Compound condition                |
| Short-circuiting | performance বাড়ায়                       | Complex decision trees            |
| Ternary Operator | এক লাইনে সিদ্ধান্ত নেয়                  | ছোট condition-based মান নির্ধারণে |
| `assert`         | condition না মানলে error তোলে           | Debugging, Testing, Validation-এ  |
