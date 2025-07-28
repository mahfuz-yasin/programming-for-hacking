
# 📘 Lesson 01: Python Introduction & Setup

## 🐍 1. Introduction to Python (What, Why, Where)
- **What**: Python একটি হাই-লেভেল, ইন্টারপ্রেটেড প্রোগ্রামিং ভাষা।
- **Why**: সহজ সিনট্যাক্স, বিশাল লাইব্রেরি, বহুমুখী ব্যবহার (Web, AI, Automation, Hacking, Game, etc.)
- **Where**:
  - Web Development: Django, Flask
  - Data Science: Pandas, NumPy
  - AI/ML: TensorFlow, scikit-learn
  - Automation: Selenium, OS module
  - Cybersecurity: Scripting, Tools
  - Game Dev: Pygame

---

## 💻 2. Installing Python & IDEs
- 🔹 Download Python: [https://python.org](https://python.org)
- 🔹 Popular IDEs:
  - **VS Code** - Lightweight, extensible
  - **IDLE** - Python built-in
  - **PyCharm** - Professional-grade IDE (Community/Pro version)

---

## ⚙️ 3. Running Python Code (CLI, File, Interpreter)
- **Interpreter (REPL mode)**:
  ```bash
  $ python
  >>> print("Hello, Python")
````

* **File Execution**:

  ```bash
  $ python hello.py
  ```
* **VS Code Shortcut**:

  * Run file: `Ctrl + Alt + N` (with Code Runner extension)

---

## 🧠 4. `__name__ == "__main__"` Explained

* বোঝায় যে স্ক্রিপ্টটি সরাসরি চালানো হয়েছে, না কি অন্য স্ক্রিপ্টে ইমপোর্ট করা হয়েছে।
* উদাহরণ:

  ```python
  def main():
      print("Running directly")

  if __name__ == "__main__":
      main()
  ```

---

## ✨ 5. The Zen of Python (PEP 20)

* Python-এর দর্শন (Philosophy) দেখতে:

  ```python
  import this
  ```
* উদাহরণ কিছু লাইন:

  ```
  Beautiful is better than ugly.
  Simple is better than complex.
  Readability counts.
  ```
