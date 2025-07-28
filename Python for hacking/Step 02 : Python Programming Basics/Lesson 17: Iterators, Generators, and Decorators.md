
# 📘 Lesson 17: Iterators, Generators, and Decorators

Python-এ **Iteration**, **Lazy Evaluation**, এবং **Function Modification** এর জন্য powerful কনসেপ্ট রয়েছে — যেমন `Iterators`, `Generators`, এবং `Decorators`। এগুলো Pythonic এবং advanced coding-এর জন্য অপরিহার্য।

---

## 🔁 1. Iterator Protocol (`__iter__`, `__next__`)

### ✅ কি?

Iterator এমন একটি object যা **একটির পর একটি element return করতে পারে**, যতক্ষণ না শেষ হয়।

Iterator-এ দুইটি বিশেষ method থাকে:

* `__iter__()` → self রিটার্ন করে
* `__next__()` → পরবর্তী item রিটার্ন করে (না থাকলে `StopIteration` তে যায়)

### ✅ কেন?

* Custom iteration behavior তৈরি করা যায়
* Memory efficient large dataset traversal

### ✅ কোথায় ব্যবহার হয়?

* Custom class কে iterable বানাতে
* For-loop বা manual iteration এ

### 🧪 উদাহরণ:

```python
class Counter:
    def __init__(self, limit):
        self.limit = limit
        self.count = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.count < self.limit:
            self.count += 1
            return self.count
        else:
            raise StopIteration

for num in Counter(3):
    print(num)
# Output: 1, 2, 3
```

---

## ⚙️ 2. Generator Functions and `yield`

### ✅ কি?

Generator হলো বিশেষ function যা `yield` keyword ব্যবহার করে **lazy iteration** করে — একসাথে সব value না দিয়ে **প্রয়োজনমতো এক একটা করে দেয়**।

### ✅ কেন?

* Huge ডেটাসেটের জন্য efficient
* Memory consumption কম
* State সংরক্ষণ করে

### ✅ কোথায় ব্যবহার হয়?

* API/DB থেকে একসাথে অনেক ডেটা না এনে এক এক করে process করার সময়
* Streams, Pipelines, Data feeds

### 🧪 উদাহরণ:

```python
def generate_numbers(n):
    for i in range(n):
        yield i

gen = generate_numbers(3)

for val in gen:
    print(val)
# Output: 0, 1, 2
```

---

## 🧲 3. Using `next()` and `StopIteration`

### ✅ কি?

* `next()` function → Iterator/Generator থেকে পরবর্তী item আনে
* `StopIteration` → যদি আর কিছু না থাকে

### ✅ কেন?

* Custom iteration কে control করা যায়
* Loop ছাড়াও manual iteration

### ✅ কোথায় ব্যবহার হয়?

* Lazy-loading বা pause-resume data access
* Explicit iteration context

### 🧪 উদাহরণ:

```python
gen = (x**2 for x in range(3))  # Generator expression

print(next(gen))  # 0
print(next(gen))  # 1
print(next(gen))  # 4
print(next(gen))  # StopIteration error
```

---

## 🎀 4. Basic Decorator Syntax and Use Cases

### ✅ কি?

**Decorator** হলো function যেটি অন্য function কে modify বা extend করে **তাকে না বদলিয়েই**।

### ✅ কেন?

* DRY Principle মানা যায় (Code Repeat না করে)
* Logging, Timing, Authorization, Access control সহজ হয়

### ✅ কোথায় ব্যবহার হয়?

* Flask/Django রুটিং
* API authentication
* Logging, Debugging

### 🧪 Syntax:

```python
def my_decorator(func):
    def wrapper():
        print("Before function")
        func()
        print("After function")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
```

➡️ Output:

```
Before function
Hello!
After function
```

---

## 🧪 Practice Exercises

1. একটি Custom Iterator তৈরি করো যা ১ থেকে ৫ পর্যন্ত সংখ্যা দেয়।
2. একটি Generator লেখো যা Fibonacci সিরিজ তৈরি করে।
3. `next()` দিয়ে একটি Generator থেকে এক এক করে মান বের করো।
4. একটি Decorator তৈরি করো যা যেকোনো ফাংশন call হওয়ার আগে ও পরে মেসেজ প্রিন্ট করে।

---

## 🧠 Summary

| বিষয়      | কি?                                 | কেন?                           | কোথায় ব্যবহার হয়?                    |
| --------- | ----------------------------------- | ------------------------------ | ------------------------------------ |
| Iterator  | Object with `__iter__` & `__next__` | Custom iteration, lazy loading | For loop, Custom iterable classes    |
| Generator | Function with `yield`               | Efficient, memory saving       | Streams, large data, lazy evaluation |
| next()    | পরবর্তী item return করে             | Manual iteration control       | Generator consumption                |
| Decorator | Function modifier (wrapper)         | Logging, auth, abstraction     | Web frameworks, code reuse           |

---