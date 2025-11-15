```markdown
# 🌍 Planet Class Project

This project fulfills all user stories for building a `Planet` class in Python.  
The goal is to validate inputs, create interactive class methods, and demonstrate object-oriented programming.

---

## 📌 User Stories Implemented

### ✔ Class Requirements
- A class named **`Planet`** exists.
- The class includes an **`__init__`** method with parameters:
  - `self`
  - `name`
  - `planet_type`
  - `star`

### ✔ Input Validation
- A **TypeError** is raised if `name`, `planet_type`, or `star` are not strings.
  - **Message:** `name, planet type, and star must be strings`
- A **ValueError** is raised if any of the strings are empty.
  - **Message:** `name, planet_type, and star must be non-empty strings`

### ✔ Attribute Assignments
Inside `__init__`:
- `self.name = name`
- `self.planet_type = planet_type`
- `self.star = star`

### ✔ Class Methods
- **`orbit()`**  
  Returns:  
``

{name} is orbiting around {star}...

``

- **`__str__()`**  
Returns:  

Planet: {name} | Type: {planet_type} | Star: {star}

`

---

## 🛠 Code Implementation

```python
class Planet:
  def __init__(self, name, planet_type, star):
      # Type checks
      if not isinstance(name, str) or not isinstance(planet_type, str) or not isinstance(star, str):
          raise TypeError("name, planet type, and star must be strings")
      
      # Empty string checks
      if name == "" or planet_type == "" or star == "":
          raise ValueError("name, planet_type, and star must be non-empty strings")

      self.name = name
      self.planet_type = planet_type
      self.star = star

  def orbit(self):
      return f"{self.name} is orbiting around {self.star}..."

  def __str__(self):
      return f"Planet: {self.name} | Type: {self.planet_type} | Star: {self.star}"
``

---

## 🌌 Planet Object Examples

The project requires creating **three instances** of the `Planet` class:

```python
planet_1 = Planet("Earth", "Terrestrial", "Sun")
planet_2 = Planet("Jupiter", "Gas Giant", "Sun")
planet_3 = Planet("Proxima b", "Exoplanet", "Proxima Centauri")
``

### 📤 Printing Planet Objects

```python
print(planet_1)
print(planet_2)
print(planet_3)
``

**Output:**

``
Planet: Earth | Type: Terrestrial | Star: Sun
Planet: Jupiter | Type: Gas Giant | Star: Sun
Planet: Proxima b | Type: Exoplanet | Star: Proxima Centauri
``

---

## 🌀 Orbit Method Output

```python
print(planet_1.orbit())
print(planet_2.orbit())
print(planet_3.orbit())
``

**Output:**

``
Earth is orbiting around Sun...
Jupiter is orbiting around Sun...
Proxima b is orbiting around Proxima Centauri...
``

---

## ✅ Tests

All required tests pass when the above implementation is used.

---

## 📚 Summary

This project demonstrates:

* Class creation
* Data validation
* Encapsulation
* Method definition
* String representation of objects

You now have a complete and fully validated `Planet` class ready for use or expansion!
