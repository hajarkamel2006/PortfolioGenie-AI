# PortfolioGenie-AI
منصة تساعد المطورين المبتدئين على إنشاء ملفات شخصية (Portfolios) احترافية وسريعة، عبر تحليل نشاطهم على GitHub وتوليد محتوى محسّن تلقائياً.
إليك الكود المباشر بلغة Markdown لملف الـ `README.md`. يمكنك نسخه بالكامل ووضعه مباشرة في ملف `README.md` على GitHub:

```markdown
# PortfolioGenie-AI 🚀

> **An AI-powered portfolio builder for developers, generated from their GitHub activity or CV.**[cite: 1]

---

##  Table of Contents
- [About The Project](#-about-the-project)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Database Architecture](#-database-architecture)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation & Setup](#installation--setup)
- [Project Scope](#-project-scope)
- [Timeline & Phases](#-timeline--phases)
- [Team Members](#-team-members)

---

##  About The Project

**PortfolioGenie-AI** is a web platform designed to help beginner developers and recent graduates quickly build a professional portfolio[cite: 2, 3]. By connecting a GitHub account, uploading a CV (PDF/DOCX), or both, the system analyzes the user's projects, coding activity, and CV content[cite: 3].

Using **AI Prompt Engineering**, PortfolioGenie automatically generates tailored project descriptions, an "About Me" section based on coding style and experience, and text optimized for SEO and readability[cite: 3].

---

##  Key Features

* **GitHub Integration:** Fetches public repositories, commit activity, and detected languages[cite: 3, 10].
* **CV Parsing:** Extracts skills, experience, and education from uploaded CVs (PDF/DOCX)[cite: 3].
* **AI Content Generation:** Generates personalized "About Me" bios and optimized project summaries[cite: 3].
* **Multi-Step Form:** Built with React Hooks (`useState`, `useEffect`) for a smooth user journey[cite: 3].
* **Live Preview & Routing:** Seamless navigation using React Router with real-time portfolio updates[cite: 3].
* **Customization & Themes:** Choose from multiple templates (Modern, Classic, Minimal) and color palettes[cite: 15, 18, 21].
* **Accessibility & SEO:** Built following web accessibility standards and SEO best practices[cite: 3].

---

##  Tech Stack

### **Front-end**
* **Framework:** React.js[cite: 2, 3]
* **Routing:** React Router[cite: 2, 3]
* **Styling:** Tailwind CSS / Custom Design System[cite: 3, 20]

### **Back-end & AI**
* **Framework:** FastAPI (Python)[cite: 17]
* **Database:** SQLite[cite: 17]
* **AI Model:** OpenAI API (Prompt Engineering)[cite: 3, 17]
* **APIs:** GitHub REST API[cite: 3]

---

##  Database Architecture

The database consists of 4 main relational tables designed to track users, portfolios, projects, and AI prompt logs[cite: 5]:


```

+---------------+        1:N        +------------------+        1:N        +---------------+
|     USERS     | ----------------> |    PORTFOLIOS    | ----------------> |   PROJECTS    |
+---------------+                   +------------------+                   +---------------+
| id (PK)       |                   | id (PK)          |                   | id (PK)       |
| github_user   |                   | user_id (FK)     |                   | portfolio_id  |
| cv_file_url   |                   | about_me         |                   | ai_description|
+---------------+                   +------------------+                   +---------------+
|                                    |
|               1:N                  |
+------------------------------------+
|
v
+---------------+
|    AI LOGS    |
+---------------+
| id (PK)       |
| prompt / resp |
+---------------+

```[cite: 5]

---

## ⚙️ Getting Started

### Prerequisites
* **Node.js** (v16.x or higher)
* **Python** (v3.10 or higher)
* **Git**

### Installation & Setup

#### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/PortfolioGenie-AI.git](https://github.com/your-username/PortfolioGenie-AI.git)
cd PortfolioGenie-AI

```

#### 2. Back-end Setup (FastAPI)

```bash
cd backend

# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the server
uvicorn main:app --reload

```

#### 3. Front-end Setup (React)

```bash
cd ../frontend

# Install dependencies
npm install

# Start development server
npm run dev

```

---

##  Project Scope

### **In Scope**



* Connecting GitHub and reading public repositories.


* Uploading CVs in PDF/DOCX format.


* Extracting skills, education, and project details.


* Interactive multi-step creation flow with live preview.


* Generative AI prompt pipeline.



### **Out of Scope**



* Portfolio hosting/domain provision.


* Private repository reading or non-GitHub platforms (GitLab/Bitbucket).


* Native mobile applications.


* Payment processing or paid subscriptions.



---

## Timeline & Phases

| Phase | Deliverable

 |
| --- | --- |
| **Week 1** | Planning, Scope & Stakeholder Analysis

 |
| **Week 2** | Design Thinking (Personas & User Journeys)

 |
| **Week 3** | UI/UX Wireframing & Design Systems

 |
| **Week 4** | ERD Design & AI Prompt Engineering

 |
| **Week 5-6** | Front-end Development (Multi-step Form & Routing)

 |
| **Week 7** | AI Integration & GitHub/CV Parsers

 |
| **Week 8** | Testing, SEO & Accessibility Refinements

 |
| **Week 9** | Final Documentation & Delivery

 |

---

 
