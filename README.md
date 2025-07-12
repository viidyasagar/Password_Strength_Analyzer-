---

# 🔐 Password Strength Analyzer with Custom Wordlist Generator

A powerful Python-based cybersecurity tool designed to **evaluate password strength** and **generate personalized wordlists** for ethical hacking, red teaming, and forensic auditing. This dual-interface tool (CLI + GUI) enhances password security awareness and supports penetration testers with targeted, realistic wordlists.

---

## 📌 Table of Contents

* [Project Overview](#-project-overview)
* [Key Features](#-key-features)
* [Technology Stack](#-technology-stack)
* [Installation](#-installation)
* [Usage Guide](#-usage-guide)

  * [Command-Line Interface (CLI)](#cli-usage)
  * [Graphical User Interface (GUI)](#gui-usage)
* [Modules Breakdown](#-modules-breakdown)
* [Sample Wordlist Outputs](#-sample-wordlist-outputs)
* [Use Cases](#-use-cases)
* [Learning Outcomes](#-learning-outcomes)
* [Screenshots](#-screenshots)
* [Contributing](#-contributing)
* [License](#-license)

---

## 📖 Project Overview

This project was developed as part of the **Elevate Labs Internship Program** to address two key areas in cybersecurity:

1. **Password Strength Analysis** – Identify weak passwords using the entropy-based `zxcvbn` algorithm.
2. **Custom Wordlist Generation** – Create dynamic, personalized wordlists based on user-provided information like name, date of birth, and pet names.

The tool aims to assist cybersecurity professionals in conducting effective penetration tests by generating context-aware password lists that mimic real-world behavior.

---

## ✨ Key Features

* 🔐 **Real-time Password Strength Evaluation** using Dropbox’s `zxcvbn` library.
* 🧠 **Custom Wordlist Generation** based on:

  * User's name, pet name, date of birth, favorite words
  * Leetspeak substitutions and year-based patterns
* 🖥️ **Dual Interface**:

  * **CLI** for advanced users
  * **GUI** for non-technical users
* 📄 **Export Wordlist** in `.txt` format for direct use in password cracking tools like Hydra, John the Ripper, or Hashcat.
* 🧩 **Modular Architecture** with separate files for analysis, generation, CLI, and GUI.

---

## ⚙️ Technology Stack

* **Language**: Python 3.13
* **Libraries**:

  * [`zxcvbn-python`](https://github.com/dropbox/zxcvbn): For password entropy evaluation
  * `tkinter`: For GUI development
  * `argparse`: For CLI argument parsing
  * Custom Python functions for mutation and wordlist generation

---

## 🧪 Installation

1. **Clone the repository:**

```bash
git clone https://github.com/your-username/password-strength-analyzer.git
cd password-strength-analyzer
```

2. **Create a virtual environment (optional but recommended):**

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies:**

```bash
pip install zxcvbn
```

---

## 🚀 Usage Guide

### ✅ CLI Usage

```bash
python cli.py --password "YourPassword123" --name "Vidyasagar" --dob "1998" --pet "Tiger"
```

#### CLI Arguments:

| Argument     | Description                     |
| ------------ | ------------------------------- |
| `--password` | Password to analyze             |
| `--name`     | User's name (used in wordlist)  |
| `--dob`      | Date of birth/year (e.g., 1998) |
| `--pet`      | Pet name (used in wordlist)     |

Output:

* Password strength feedback
* Estimated crack time
* Custom wordlist saved as `wordlist.txt`

---

### 🖥 GUI Usage

```bash
python gui.py
```

* Simple form to enter password and personal details
* Click "Analyze" to view password strength
* Click "Generate Wordlist" to save a custom `.txt` file

---

## 🧩 Modules Breakdown

| File           | Description                        |
| -------------- | ---------------------------------- |
| `analyzer.py`  | Handles password strength analysis |
| `generator.py` | Wordlist generation and mutations  |
| `cli.py`       | Command-line interface logic       |
| `gui.py`       | GUI built using tkinter            |

---

## 📂 Sample Wordlist Outputs

Example output (`wordlist.txt`) for input:

* Name: `Vidyasagar`
* DOB: `1998`
* Pet: `Tiger`

```text
vidyasagar
tiger1998
T1g3r
vidya@1998
V1dy@s@g@r
t1g3r_98
...
```

---

## 🧭 Use Cases

* 🛡 Penetration Testing
* 🔎 Digital Forensics
* 🧪 Password Security Research
* 📚 Cybersecurity Education and Awareness

---

## 🎓 Learning Outcomes

This project provided real-world experience in:

* Implementing secure password auditing methods
* Designing tools for ethical hacking
* GUI development with `tkinter`
* Working with password entropy algorithms
* Writing clean, modular, and extensible Python code

---

## 🖼 Screenshots

<sub>Add screenshots of GUI and CLI outputs here (optional)</sub>

---

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request with improvements.

---

## 📜 License

This project is licensed under the MIT License.

---

Let me know if you'd like this written to a `README.md` file directly or want me to generate GUI screenshots or demo GIFs for your project.

