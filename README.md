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
## 🚀 Commands Cheat Sheet

| Command               | Purpose                                       |
|------------------------|-----------------------------------------------|
| `rasa init`            | Creates the project and trains initial model  |
| `rasa train`           | Retrains the model after changes              |
| `rasa shell`           | Talk to the bot in the terminal               |
| `rasa shell nlu`       | Test NLU understanding of intents/entities    |
| `rasa run actions --debug`| To start the action server                 |



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
### ✅ 6. To have a conversation with the bot in cmd
```bash
rasa shell
```
to exit the conversation `CTRL+C`

---
---

## 🔄 Project Updates Summary

This section summarizes all updates made to the Rasa chatbot across different files.

---

### 📄 `nlu.yml` – Intents and Training Examples

#### Intents Added:
  - greet
  - goodbye
  - affirm
  - deny
  - mood_great
  - mood_unhappy
  - bot_challenge
  - ask_price
  - inquire_model
  - schedule_test_drive
  - ask_features
  - ask_dealership
  - ask_warranty
  - ask_maintenance
  - ask_availability


---

### 📄 `domain.yml` – Bot Configuration

#### Intents:
  - greet
  - goodbye
  - affirm
  - deny
  - mood_great
  - mood_unhappy
  - bot_challenge
  - ask_price
  - inquire_model
  - schedule_test_drive
  - ask_features
  - ask_dealership
  - ask_warranty
  - ask_maintenance
  - ask_availability

#### Entities:
- `car_model`
- `car_make`

#### Slots:
-`car model`
`car_make`

#### Responses:
- utter_greet
- utter_goodbye
- utter_cheer_up
- utter_did_that_help
- utter_happy
- utter_iamabot
- utter_ask_car_model
- utter_provide_car_price
- utter_available_models
- utter_confirm_test_drive
- utter_features_info
- utter_dealership_info
- utter_warranty_info
- utter_maintenance_info
- utter_availability_info



#### Actions:
  - action_show_available_models ( it show all the models using nhtsa vehicle API)
  - action_provide_car_price
  - action_handle_test_drive

---

### 📄 `stories.yml`
- **show car models** it uses the [intent:inquire_model] [actions: utter_ask_car_make , action_show_available_models]
- 


---
## Requirements

- Python 3.8
- Rasa (latest version compatible)
- Anaconda
- Visual Studio Code (recommended for editing or any IDE)







