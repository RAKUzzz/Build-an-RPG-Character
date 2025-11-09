# 🧙‍♂️ Character Creator (Python)

A simple character creation program built in Python.  
This project was part of my learning journey to practice **input validation**, **string manipulation**, and **f-strings**.  

---

## 💡 Overview

The function `create_character()` validates the player's input (name and stats)  
and returns a visual representation of the character’s stats using filled (`●`) and empty (`○`) symbols.

---

## 🧩 Features

✅ Validate that the name:
- Is a string  
- Contains no spaces  
- Is no longer than 10 characters  

✅ Validate that all stats (`strength`, `intelligence`, `charisma`):
- Are integers  
- Have values between **1** and **4**  
- Add up exactly to **7 points total**  

✅ Returns a text-based “status card” of the character’s attributes.

---

## 🧠 Example

```python
def create_character(name, strength, intelligence, charisma):
    if not isinstance(name, str):
        return 'The character name should be a string'
    if len(name) > 10:
        return 'The character name is too long'
    if ' ' in name:
        return 'The character name should not contain spaces'
    if not isinstance(strength, int) or not isinstance(intelligence, int) or not isinstance(charisma, int):
        return 'All stats should be integers'
    if strength < 1 or intelligence < 1 or charisma < 1:
        return 'All stats should be no less than 1'
    if strength > 4 or intelligence > 4 or charisma > 4:
        return 'All stats should be no more than 4'
    if strength + intelligence + charisma != 7:
        return 'The character should start with 7 points'
    return f"{name}\nSTR {'●' * strength}{'○' * (10 - strength)}\nINT {'●' * intelligence}{'○' * (10 - intelligence)}\nCHA {'●' * charisma}{'○' * (10 - charisma)}"

```

## 🚀 What I Learned
- How to use isinstance() for type checking
- How to handle logical conditions and validation
- How to use f-strings with \n for clean multiline output
- How to use string multiplication to create visual “bar indicators”

---

## ✨ Author
Methawin Srivilai  
Built as part of my Python learning journey toward becoming a Software Engineer.
