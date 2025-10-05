# 🛡️ N8N Automation: Automated Credentials Backup to GitHub

## 🚀 Project Overview

This repository hosts an n8n workflow specifically designed for **automated, scheduled backup** of your n8n **Credentials** to a private GitHub repository.

While backing up workflows is common, securing your credentials (API keys, tokens, etc.) is critical for quick disaster recovery. This workflow ensures that your sensitive data is exported in an **encrypted format** and committed to version control. 

---

## ✨ Key Features (Workflow Logic)

Цей робочий процес є критичним для інфраструктури, оскільки він виконує три основні завдання:

1.  **Credentials-Focused Export:** Використовує вузол **`Execute Command`** для виконання команди `n8n export:credentials` на вашій інстанції.
2.  **Encryption Validation:** Експортований файл JSON містить **зашифровані** облікові дані, забезпечуючи, що сирі секрети не зберігаються в репозиторії.
3.  **GitHub Commitment:** Використовує вузли **`GitHub`** для автоматичного створення комміту (commit) з оновленим файлом резервної копії, надаючи версійний контроль.

### Схематичний вигляд робочого процесу (Simplified Flow)
