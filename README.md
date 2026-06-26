<div align="center">

# 🌿 Greenify

**A playful GitHub Contribution Graph demonstration tool**

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)](https://git-scm.com)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

</div>

---

## 🎯 What is Greenify?

Greenify is an **educational Python script** that demonstrates how Git timestamps work and how GitHub calculates contribution graphs. It generates a local Git repository with backdated commits to illustrate the mechanics of Git history and GitHub's activity tracking.

> ⚠️ **Disclaimer:** This tool is for **educational and demonstrative purposes only**. It is intended to help developers understand Git internals and GitHub contribution mechanics. Please do not use it to misrepresent your actual development activity.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🎲 **Randomized Activity** | Configurable commit frequency and density |
| 📅 **Flexible Date Range** | Customizable days before/after current date |
| 🏖️ **Weekend Skip** | Option to exclude weekends for realistic patterns |
| 🚀 **One-Command Push** | Automatically push to your GitHub repository |
| ⚡ **Fast & Lightweight** | Pure Python, no external dependencies |

---

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Git installed
- A GitHub account

### Installation

```bash
# Clone this repository
git clone https://github.com/Faraysz/Greenify.git
cd Greenify

# Run the script
python main.py --repo=./my-repo --days=365 --max-commits=8 --frequency=60
```

### Usage Examples

```bash
# Basic usage (local only)
python main.py --repo=./fake-repo --days=365

# With GitHub push
python main.py --repo=./fake-repo --days=365 --remote=https://github.com/username/repo.git

# Skip weekends, higher frequency
python main.py --repo=./fake-repo --days=365 --max-commits=12 --frequency=80 --no-weekends
```

### Available Options

| Argument | Default | Description |
|----------|---------|-------------|
| `--repo` | *(required)* | Path to local repository folder |
| `--remote` | `None` | Remote GitHub URL (optional) |
| `--days` | `365` | Number of days to generate commits for |
| `--max-commits` | `10` | Maximum commits per day |
| `--frequency` | `70` | Percentage of days to commit (0-100) |
| `--no-weekends` | `False` | Skip Saturday and Sunday |

---

## 🖼️ Preview

**Before:** A sparse contribution graph with minimal activity.

**After:** A rich, consistent contribution timeline demonstrating the power of Git's date manipulation features.

---

## 🛠️ How It Works

1. **Initialize** a local Git repository
2. **Generate** a dummy file (`activity.txt`) with timestamped entries
3. **Create** commits with backdated `GIT_AUTHOR_DATE` and `GIT_COMMITTER_DATE`
4. **Push** the entire history to your GitHub repository
5. **GitHub reindexes** the commits and reflects them on your contribution graph

---

## 📂 Project Structure

```
Greenify/
├── main.py          # Main script
├── README.md        # This file
└── .gitignore       # Ignore cache & temp files
```

---

## ⚠️ Important Notes

- GitHub may take **5–10 minutes** to reindex and display new contributions
- Ensure your local Git email matches your GitHub email:
  ```bash
  git config --global user.email "your-github@email.com"
  ```
- Private repository contributions only appear if enabled in [GitHub Settings](https://github.com/settings/profile)

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request if you have ideas for improvements.

---

## 📜 License

This project is licensed under the **MIT License**.

---

<div align="center">

Built with 💚 by [Faraysz](https://github.com/Faraysz)

</div>
