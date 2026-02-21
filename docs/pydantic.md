# Pydantic - High Level Overview

## 📌 What is Pydantic
- Python library for **data validation + parsing**
- Uses **type hints** to enforce data correctness
- Automatically converts input data into expected types

👉 Think: **DTO + Validation + Parsing (like Java Bean Validation + Jackson)**

---

## ❌ What if we don't use Pydantic
- Manual validation everywhere
- Type conversion handled manually
- More bugs due to invalid inputs
- Repetitive boilerplate code

---

## ⚠️ Pain Points Without Pydantic
- ❌ No central validation logic
- ❌ Runtime errors (wrong types)
- ❌ Complex nested data handling
- ❌ Hard to maintain API input validation
- ❌ Inconsistent error handling

---

## ✅ Where Mostly Used
- FastAPI (request/response validation)
- Data pipelines (clean input data)
- ML / AI preprocessing
- Config management
- Parsing JSON / external API data

---

## 🔹 Basic Example

### Without Pydantic
```python
data = {"name": "Subbu", "age": "25"}

if not isinstance(data["age"], int):
    data["age"] = int(data["age"])  # manual conversion

if data["age"] < 0:
    raise ValueError("Invalid age")