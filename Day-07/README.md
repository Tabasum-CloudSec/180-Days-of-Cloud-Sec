# 🛡️ Day 07: Linux Provisioning & Tool Management

## 📋 Overview
Day 07 focuses on **System Provisioning**—the process of fetching and managing professional security software. Understanding the hierarchy of package managers is crucial for maintaining a stable penetration testing environment.

---

## 🏗️ 1. The Package Hierarchy: Worker vs. Manager

### 📦 Low-Level: `dpkg` (The Worker)
* **Role:** Directly installs individual `.deb` files.
* **Limitation:** Offline tool; it cannot resolve "Dependency Hell" (missing prerequisite files).
* **Command:**
    ```bash
    sudo dpkg -i package_name.deb
    ```

### 🌐 High-Level: `APT` (The Manager)
* **Role:** The standard tool for installing, updating, and removing software.
* **Logic:** Connects to online **Repositories** and automatically resolves dependencies.
* **Command:**
    ```bash
    sudo apt update && sudo apt install [tool_name]
    ```

---

## 🔗 2. GitHub: Source Code & Version Control

### 📋 Overview
When tools are unavailable in official repositories, we use **Git** to pull source code directly from developers.

### 🏗️ Why Git?
1.  **Direct Access:** Access the tool's raw source code (DNA).
2.  **Bleeding Edge:** Get updates immediately before they hit official stores.
3.  **Automation:** Clone entire projects into your terminal instantly.

### 🛠️ Essential Command
```bash
git clone https://github.com/user/tool-name.git
```

---

## 🐍 3. Python PiP: The Script Doctor

### 📋 Overview
**PiP** is a specialized manager for Python libraries. Since ~80% of hacking scripts are Python-based, PiP is essential for resolving environment errors.

### 🏗️ Why PiP?
It fixes the common `ImportError: No module named 'library_name'` by installing the specific Python "ingredients" required for a script to execute.

### 🛠️ Essential Command
```bash
pip install [module_name]
# Example: pip install requests
```

---
*Status: Day 07 Completed | Learning Linux Provisioning for Cyber Security.*
