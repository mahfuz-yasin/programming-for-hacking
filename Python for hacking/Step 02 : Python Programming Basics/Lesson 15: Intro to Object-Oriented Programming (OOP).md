
# 📘 Lesson 15: Intro to Object-Oriented Programming (OOP)

**Object-Oriented Programming (OOP)** একটি প্রোগ্রামিং পদ্ধতি যেখানে প্রোগ্রামিং উপাদানগুলোকে **অবজেক্ট** এবং **ক্লাস** আকারে সংগঠিত করা হয়। এটি বড় প্রজেক্ট, মডুলার ডিজাইন, এবং কোড রিইউজেবিলিটির জন্য গুরুত্বপূর্ণ।

---

## 🧱 1. Class and Object

### 📌 কি?

* **Class**: একটি ব্লুপ্রিন্ট বা কাঠামো যা থেকে অবজেক্ট তৈরি হয়।
* **Object**: ক্লাস থেকে তৈরি কনক্রিট instance যা তথ্য ও ফাংশন ধারণ করে।

### 📌 কেন?

* Data ও function একত্রে ব্যবস্থাপনার জন্য
* বড় প্রজেক্টকে manageable অংশে ভাগ করার জন্য
* কোড পুনঃব্যবহার (Reusability)

### 📌 কোথায় ব্যবহার হয়?

* গেম ডেভেলপমেন্টে (e.g., Player, Enemy)
* ওয়েব অ্যাপে (e.g., User, Product, Cart)
* বড় সফটওয়্যার আর্কিটেকচারে

### ✅ উদাহরণ:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("Mahfuz", 25)
print(person1.name)  # Mahfuz
```

---

## 🛠️ 2. `__init__()` Constructor

### 📌 কি?

* `__init__()` হলো ক্লাসের constructor method যা অবজেক্ট তৈরি হওয়ার সময় স্বয়ংক্রিয়ভাবে চলে।

### 📌 কেন?

* Object তৈরি করার সময় কিছু প্রাথমিক মান সেট করতে

### 📌 কোথায় ব্যবহার হয়?

* যখন Object তৈরি হতেই নির্দিষ্ট attributes থাকতে হয়

### ✅ উদাহরণ:

```python
class Student:
    def __init__(self, name, roll):
        self.name = name
        self.roll = roll
```

---

## 🧮 3. Instance vs Class Variables

### 📌 কি?

* **Instance Variable**: প্রতিটি object-এর জন্য আলাদা মান
* **Class Variable**: সব object-এর জন্য একটি common মান

### 📌 কেন?

* কিছু বৈশিষ্ট্য অবজেক্ট-ভিত্তিক (instance), আবার কিছু ক্লাস-ভিত্তিক (class-wide)

### 📌 কোথায় ব্যবহার হয়?

* Class-wide setting (e.g., default\_tax\_rate)
* Object-specific data (e.g., user.name)

### ✅ উদাহরণ:

```python
class Employee:
    company = "TechCorp"       # class variable

    def __init__(self, name):
        self.name = name       # instance variable

emp1 = Employee("Alice")
print(emp1.company)  # TechCorp
```

---

## 🧰 4. Methods (instance, class, static)

### 📌 কি?

| Method Type     | প্রথম আর্গুমেন্ট | Access কী করে          |
| --------------- | ---------------- | ---------------------- |
| Instance Method | `self`           | অবজেক্ট দিয়ে           |
| Class Method    | `cls`            | ক্লাস দিয়ে             |
| Static Method   | None             | Utility হিসেবে কাজ করে |

### 📌 কেন?

* ভিন্ন ভিন্ন টাইপের behavior কে আলাদা করার জন্য

### 📌 কোথায় ব্যবহার হয়?

* Instance Method → object-specific কাজের জন্য
* Class Method → class-level data পরিবর্তনের জন্য
* Static Method → utility বা calculation ফাংশনের জন্য

### ✅ উদাহরণ:

```python
class Math:
    @staticmethod
    def add(x, y):
        return x + y

print(Math.add(3, 4))  # 7
```

---

## 🧬 5. Inheritance and Polymorphism

### 📌 কি?

* **Inheritance**: একটি ক্লাস আরেকটি ক্লাসের বৈশিষ্ট্য গ্রহণ করে।
* **Polymorphism**: একই নামের method ভিন্ন ক্লাসে ভিন্নভাবে কাজ করে।

### 📌 কেন?

* কোড পুনর্ব্যবহার ও একাধিক ক্লাসে একই interface রাখতে

### 📌 কোথায় ব্যবহার হয়?

* Base class → Animal, Subclass → Dog, Cat
* Override → `speak()` method প্রতিটি subclass-এ ভিন্ন আচরণে

### ✅ উদাহরণ:

```python
class Animal:
    def speak(self):
        print("Makes sound")

class Dog(Animal):
    def speak(self):
        print("Bark")

a = Dog()
a.speak()  # Output: Bark
```

---

## 🧪 Practice Exercises

1. একটি `Car` ক্লাস তৈরি করো যার মধ্যে `__init__`, `start()` method থাকবে।
2. `Employee` ক্লাসে `company` কে class variable হিসেবে রাখো, এবং employee-specific data রাখো instance variable এ।
3. `Math` ক্লাসে `@staticmethod` দিয়ে `multiply(a, b)` method তৈরি করো।
4. `Animal` → `Bird` → `speak()` override করে polymorphism বুঝাও।

---

## 🧠 Summary

| বিষয়                         | উদ্দেশ্য                            |
| ---------------------------- | ----------------------------------- |
| Class/Object                 | Code Structure ও রিইউজেবিলিটি       |
| `__init__()`                 | Object তৈরির সময় মান সেট            |
| Instance/Class Var           | Data নির্দিষ্ট বা শেয়ারড রাখার উপায় |
| Instance/Class/Static Method | কাজের ধরন অনুযায়ী method ভাগ        |
| Inheritance                  | Behavior reuse ও hierarchy          |
| Polymorphism                 | Overridden method এর বৈচিত্র্য      |

---