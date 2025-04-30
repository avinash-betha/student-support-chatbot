# AI Chatbot for Student Support

This is a demo intelligent assistant built using **Rasa** to simulate a student support chatbot experience. It helps students with academic queries and collects basic information through a web-based conversational interface. This project is for educational and demonstration purposes only.

---

## Features

- Collects student name, ID, major, and email via form
- Handles real-time course and academic FAQs
- Clean, floating-button (FAB) web UI built with HTML/CSS/JS
- Rule-based form logic and intent classification using Rasa
- Autoscroll, responsive design, and professional UX

---

## Project Structure

```
student-support-chatbot/
├── actions.py              # Custom actions (currently minimal)
├── data/
│   ├── nlu.yml             # Intent training examples
│   ├── rules.yml           # Rules for handling flows
│   └── stories.yml         # Optional story support
├── domain.yml              # Slot, form, and response definitions
├── endpoints.yml           # Action server endpoint
├── credentials.yml         # Channels (REST enabled)
├── config.yml              # NLU pipeline and policies
├── index.html              # Web UI with FAB chat window
├── .gitignore
└── README.md
```

---

## How to Run

> Ensure Python 3.8 or 3.10 and virtualenv are installed

### 1. Create virtual environment

```bash
python -m venv venv
source venv/bin/activate   # or venv\\Scripts\\activate on Windows
```

### 2. Install dependencies

```bash
pip install rasa firebase-admin
```

> (Skip Firebase if not used)

### 3. Train model

```bash
rasa train
```

### 4. Run Rasa server (with CORS for web chat)

```bash
rasa run --enable-api --cors "*"
```

### 5. (Optional) Run action server

```bash
rasa run actions
```

### 6. Launch Web UI

Open `index.html` in your browser — it will load the floating chatbot.

---

## Intents Handled

- `ask_available_courses`
- `ask_registration_process`
- `ask_professor_contact`
- `ask_department_office`
- `ask_academic_calendar`
- `ask_tuition_payment`
- `ask_scholarships`

---

## Future Enhancements

- Store form data in Firebase or SQL
- Admin dashboard to view submitted students
- Deploy chatbot on WhatsApp, Telegram, or as mobile PWA

---

## Developed By

**Avinash Betha**  
MS in Data Science  
Built as a smart university support chatbot demo project using Rasa.
