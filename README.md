# Rasa-Car-sales-Chatbot

A simple AI chatbot built using Rasa for handling car sales conversations — including greeting users, showing available car models, answering FAQs, checking prices, and scheduling test drives.

---

## 📁 Project Structure

This project was created using `rasa init`. The key folders/files include:

- `data/nlu.yml` – Intent examples for training the NLU
- `data/rules.yml` and `data/stories.yml` – Define the dialogue flows
- `domain.yml` – Contains intents, responses, entities, slots, and actions
- `actions.py` – File for custom Python actions (if any)
- `models/` – Stores trained models
- `config.yml` – ML pipeline and policy configuration

---

## 🛠️ Setup Instructions (Using Anaconda)

> ⚠️ Rasa works best with Python 3.7–3.10. Higher versions like Python 3.12 may not be supported.

### ✅ 1. Open Anaconda Prompt

Create a virtual environment with Python 3.8:

```bash
conda create -n rasa_bot python=3.8
```
### ✅ 2. Activate the environment
```bash
conda activate rasa_bot
```
### ✅ 3. Install Rasa
```bash
pip install rasa
```
### ✅ 4. Initialize the Rasa project
```bash
rasa init
```
This will:
- Generate the folder structure
- Create training data and responses
- Train an initial model
- Launch an optional interactive test

---

### ✅ 5. Open the project in VS Code

After initializing:
- Open **VS Code**
- Go to `File > Open Folder` and select the chatbot project folder
- Open the **Command Palette** (`Ctrl + Shift + P`)
- Select: `Python: Select Interpreter`
- Choose the interpreter from `rasa_bot` environment (e.g., `conda-env:rasa_bot`)

---
### ✅ 6. Train the bot

Use this command anytime you modify intents or stories:
```bash
rasa train
```









