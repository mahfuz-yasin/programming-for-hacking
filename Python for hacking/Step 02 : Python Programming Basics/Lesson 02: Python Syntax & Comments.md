
## 🧱 1. Python Syntax Structure
- Python একটি **syntax-friendly** language যার কোড পড়া এবং লেখা সহজ।
- Code blocks `{}` ব্যবহার না করে **indentation**-এর উপর নির্ভর করে।
- উদাহরণ:
  ```python
  print("Hello World")      # Valid
  x = 5 + 3 * 2             # Operators follow mathematical rules
````

---

## 🔠 2. Indentation Rules

* Python-এ কোড ব্লকের শুরু ও শেষ নির্ধারণ হয় **indentation** দিয়ে।
* সাধারণত ৪টি স্পেস (বা একটি ট্যাব) ব্যবহার করা হয়।
* ভুল ইনডেন্টেশন হলে `IndentationError` হবে।

✅ সঠিক উদাহরণ:

```python
if True:
    print("Indented properly")
```

❌ ভুল উদাহরণ:

```python
if True:
print("This will throw error")  # IndentationError
```

---

## 💬 3. Comments (Single line, Multi-line)

### ➤ Single-line Comments:

* `#` দিয়ে শুরু হয়

```python
# This is a single-line comment
x = 5  # Inline comment
```

### ➤ Multi-line Comments:

* একাধিক লাইনে `#` ব্যবহার করতে হয়

```python
# This is a
# multi-line comment
```

---

## 📝 4. Docstrings (Function Documentation)

* ফাংশনের জন্য **documentation/comment block** হিসেবে ব্যবহৃত হয়।
* Triple quotes `""" """` বা `''' '''` দিয়ে লেখা হয়।
* Access করা যায়: `function_name.__doc__`

```python
def greet(name):
    """
    This function greets the user.
    :param name: str
    :return: None
    """
    print(f"Hello, {name}")
```

```python
print(greet.__doc__)
```
