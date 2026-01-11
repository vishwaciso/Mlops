# 🐍 Python Modules, Packages & Libraries – From Scratch (Complete Guide)

> **Beginner → Advanced | GitHub + PyPI Ready | Interview + Teaching Friendly**

This README explains **what modules, packages, and libraries are**, **how to create them from scratch**, and **how they are used in real-world projects**, with **clear visuals and folder structures**.

---

## 📌 TABLE OF CONTENTS
1. What is a Module?
2. What is a Package?
3. What is a Library?
4. Visual Comparison (Module vs Package vs Library)
5. Creating a Python Module (From Scratch)
6. Creating a Python Package (From Scratch)
7. Creating a Python Library (Industry Standard)
8. Real-Time Folder Structure
9. How Import Works Internally
10. Common Mistakes & Best Practices
11. Interview & Real-Time Mapping

---

## 1️⃣ What is a Python Module?

### ✅ Definition
A **module** is a **single Python file (`.py`)** that contains:
- functions
- classes
- variables

### 📌 Example
```python
# math_utils.py

def add(a, b):
    return a + b
```

### ✅ Usage
```python
import math_utils
math_utils.add(2, 3)
```

### 🔑 Key Points
- One file = one module
- Used to organize code
- Smallest reusable unit

---

## 2️⃣ What is a Python Package?

### ✅ Definition
A **package** is a **folder** that contains:
- one or more modules
- an `__init__.py` file

### 📌 Example Structure
```
finance/
│── __init__.py
│── tax.py
│── salary.py
```

### 📌 Example Code
```python
# finance/tax.py

def calculate_tax(amount):
    return amount * 0.18
```

### ✅ Usage
```python
from finance.tax import calculate_tax
```

### 🔑 Key Points
- Folder = package
- Groups related modules
- Improves maintainability

---

## 3️⃣ What is a Python Library?

### ✅ Definition
A **library** is a **complete project** that contains:
- multiple packages
- configuration files
- documentation
- ready to install using `pip`

### 📌 Example Libraries
- numpy
- pandas
- scikit-learn

### 🔑 Key Points
- Libraries are **published** (PyPI)
- Installed via `pip install`
- Used across projects

---

## 4️⃣ VISUAL COMPARISON (VERY IMPORTANT)

```
┌────────────┐
│  MODULE    │
│  (.py)     │
└─────┬──────┘
      ↓
┌────────────┐
│  PACKAGE   │
│  (folder)  │
│  modules   │
└─────┬──────┘
      ↓
┌────────────┐
│  LIBRARY   │
│  (project) │
│  packages  │
└────────────┘
```

---

## 5️⃣ Creating a Python Module (Step-by-Step)

### 🔹 Step 1: Create File
```bash
touch calculator.py
```

### 🔹 Step 2: Write Code
```python
# calculator.py

def multiply(a, b):
    return a * b
```

### 🔹 Step 3: Use Module
```python
import calculator
calculator.multiply(2, 4)
```

---

## 6️⃣ Creating a Python Package (Step-by-Step)

### 🔹 Step 1: Create Folder
```bash
mkdir monitoring
cd monitoring
touch __init__.py alerts.py metrics.py
```

### 📁 Structure
```
monitoring/
│── __init__.py
│── alerts.py
│── metrics.py
```

### 🔹 Step 2: Add Code
```python
# alerts.py

def send_alert():
    return "Alert sent"
```

### 🔹 Step 3: Import Package Module
```python
from monitoring.alerts import send_alert
```

---

## 7️⃣ Creating a Python Library (REAL INDUSTRY WAY)

### 📁 Library Structure
```
infra-toolkit/
│
├── grc/
│   ├── __init__.py
│   ├── compliance.py
│   └── risk.py
│
├── soc/
│   ├── __init__.py
│   ├── monitoring.py
│   └── alerts.py
│
├── pyproject.toml
├── README.md
```

### 📌 Library Name (PyPI)
```
infra-toolkit
```

### 📌 Packages Inside
```
grc, soc
```

### 📌 Modules Inside
```
compliance.py, risk.py, monitoring.py, alerts.py
```

---

## 7️⃣A Enterprise Real-Time Example (GRC + SOC)

### 🏢 Scenario: Enterprise Cloud Security Platform

A company wants a **single reusable Python library** for:
- Governance & Compliance (GRC)
- Security Operations Center (SOC)

Instead of writing scripts again and again, they build a **library**.

### 📦 GRC Package (Governance & Risk)
```python
# grc/compliance.py

def check_iso27001():
    return "ISO 27001 controls validated"
```

```python
# grc/risk.py

def calculate_risk(score):
    if score > 7:
        return "High Risk"
    return "Low Risk"
```

### 📦 SOC Package (Monitoring & Alerts)
```python
# soc/monitoring.py

def detect_intrusion():
    return "No intrusion detected"
```

```python
# soc/alerts.py

def send_soc_alert():
    return "SOC alert triggered"
```

### 🔹 How Enterprise Teams Use It
```python
from grc.compliance import check_iso27001
from soc.monitoring import detect_intrusion
```

👉 Same library used by:
- GRC team
- SOC analysts
- DevSecOps pipelines

---

## 8️⃣ How `pip install` Works (Internals)

```
pip install infra-toolkit
        ↓
Downloads from PyPI
        ↓
Installs packages into site-packages
        ↓
You import packages/modules
```

```python
from grc.compliance import check_iso27001
```

---

## 8️⃣A Publishing Library to PyPI (Step-by-Step)

### 🔹 Step 1: Install Build Tools
```bash
pip install build twine
```

### 🔹 Step 2: Create `pyproject.toml`
```toml
[build-system]
requires = ["setuptools>=61.0"]
build-backend = "setuptools.build_meta"

[project]
name = "infra-toolkit"
version = "0.1.0"
description = "Enterprise GRC and SOC automation toolkit"
authors = [{name="Vishwanath"}]
readme = "README.md"
requires-python = ">=3.8"
```

### 🔹 Step 3: Build Library
```bash
python -m build
```

### 🔹 Step 4: Upload to PyPI
```bash
twine upload dist/*
```

### 🔹 Step 5: Install Anywhere
```bash
pip install infra-toolkit
```

👉 This is how **real companies publish internal & public libraries**.

---

## 9️⃣ Common Mistakes ❌

| Mistake | Why Wrong |
|------|----------|
| python -m . | Library root is not executable |
| Missing __init__.py | Package not detected |
| project.toml | Should be pyproject.toml |
| Running library | Libraries are imported, not run |

---

## 🔟 Best Practices ✅

- One responsibility per module
- Group related modules into packages
- Use meaningful names
- Always add README.md
- Follow semantic versioning (VERY IMPORTANT)

---

## 🔢 Versioning & Upgrade Strategy (0.1.0 → 1.0.0)

Python libraries follow **Semantic Versioning (SemVer)**:

```
MAJOR.MINOR.PATCH
```

### 🔹 Version Meaning

| Version Part | Meaning | Example |
|-------------|--------|---------|
| MAJOR | Breaking changes | 1.0.0 → 2.0.0 |
| MINOR | New features (backward compatible) | 1.1.0 |
| PATCH | Bug fixes only | 1.1.1 |

---

### 🚧 Early Development Phase (0.x.x)

```
0.1.0 → 0.2.0 → 0.5.0
```

Used when:
- Library is evolving
- APIs may change
- Used internally or by early adopters

Example:
```toml
version = "0.1.0"
```

---

### 🚀 Stable Release (1.0.0)

You release **1.0.0** when:
- Public APIs are stable
- Documentation is complete
- No breaking changes expected

```toml
version = "1.0.0"
```

👉 This signals **production readiness**.

---

### 🔄 Upgrade Scenarios (Real-Time)

#### ✅ Patch Update
```
1.0.0 → 1.0.1
```
- Bug fix
- No API changes

#### ✅ Minor Update
```
1.0.0 → 1.1.0
```
- New module added
- Backward compatible

#### ❌ Major Update
```
1.0.0 → 2.0.0
```
- Function signature changes
- Module renamed or removed

---

### 🏢 Enterprise Upgrade Strategy

Best practice:
- Lock versions in production

```bash
pip install infra-toolkit==1.0.0
```

- Upgrade in staging first
- Read CHANGELOG before upgrade

---

### 📄 Recommended: CHANGELOG.md

```md
## [1.0.0] - Stable Release
- Initial stable API
- GRC and SOC packages finalized

## [0.2.0]
- Added SOC alerting module

## [0.1.0]
- Initial beta release
```

---

## 🎯 Interview Mapping (VERY IMPORTANT)

| Question | Answer |
|-------|------|
| What is module? | Single .py file |
| What is package? | Folder of modules |
| What is library? | Installable project |
| pip installs what? | Library |
| import accesses? | Package / module |

---

## 🚀 FINAL ONE-LINE SUMMARY

> **Module = file**  
> **Package = folder**  
> **Library = project published to PyPI**

---

📌 **Perfect for GitHub, YouTube teaching, interviews, and real-world usage**

---

👨‍🏫 Created for learners who want **clarity, not confusion**

