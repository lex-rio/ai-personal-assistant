## 📘 Documentation Structure for Personal AI Assistant

A system that orchestrates various LLM access accounts or different LLM models (hereinafter referred to as *assistants*) will help organize household, work, health, etc. Multiple assistants are needed to avoid the limitations of the free context window. The context is stored locally on hardware in the form of a knowledge base (Obsidian notes and a relational database). If any assistant lacks certain data, it can access the knowledge base using Retrieval-Augmented Generation (RAG). As an LLM provider, one can try DeepSeek since it provides the largest context window among all free options.

---

### 1. 🎯 Introduction

- **Project Goal**:
  Create a personal AI assistant that helps manage information, planning, health, finances, and other aspects of daily life.

- **Main Advantages**:
  Automation of routine tasks, increased productivity, personalized advice, data privacy preservation.

---

### 2. 🧠 Roles of Assistants

Each assistant is responsible for a specific area and interacts with relevant data sources.

#### 2.1. 📬 Email Assistant
- **Functions**: Analyzes emails, summarizes important points, suggests draft responses.
- **Integrations**: Email, calendar.

#### 2.2. 🧘 Psychological Assistant
- **Functions**: Emotional check-ins, daily reflections, mental health advice.
- **Integrations**: Obsidian, psychology knowledge base.

#### 2.3. ⏰ Reminder Assistant
- **Functions**: Reminders for tasks, deadlines, personal matters. Once a week, the program analyzes the vault and tries to "revisit" topics that haven’t been mentioned, asking the LLM "do you remember this project?" — and if not, generates a digest with old notes.
- **Integrations**: Calendar, Telegram.

#### 2.4. 📅 Event Analyst/Planner
- **Functions**: Daily/weekly dialogue "let’s summarize yesterday — plan for tomorrow" based on Tasks and Vault, task balancing.
- **Integrations**: Obsidian, calendar, task list.

#### 2.5. 🏋️ Health and Sports Assistant
- **Functions**: Recommendations for nutrition, workouts, habit tracking.
- **Integrations**: Fitness apps, nutrition data, financial assistant.

#### 2.6. 📰 RSS Digest
- **Functions**: Collects news from RSS, filters topics, sends digests.
- **Integrations**: RSS feeds, Telegram.

#### 2.7. 🍽️ Recipe Assistant
- **Functions**: Suggests recipes based on available ingredients, maintains a grocery list.
- **Integrations**: Shopping lists, health assistant, Obsidian.

#### 2.8. 💰 Financial Assistant
- **Functions**: Analyzes bank statements, manages budget, plans expenses.
- **Integrations**: Bank statements in CSV/JSON, Obsidian, nutrition assistant.

#### 2.9. 🤝 Social Assistant
- **Functions**: Reminds about birthdays, suggests gift ideas, analyzes social connections.

#### 2.10. 🌍 Travel Assistant
- **Functions**: Plans trips, books tickets, creates itineraries considering budget and health.

---

### 3. 🔌 Integrations

Describes the interaction of assistants with systems.

- **Obsidian**: Central repository for personal knowledge.
- **Calendar**: Synchronization of events, reminders, planning.
- **Telegram**: Interface for interaction and notifications.
- **Email**: Source of daily incoming events and tasks.
- **Banking Tools**: Export formats (CSV/JSON) for analysis.

---

### 4. 🧱 System Architecture

- **Components**: AI agents, knowledge bases, interfaces.
- **Communication**: Event-driven or scheduled exchange between agents.
- **Security**: Local data storage, restricted access.

---

### 5. ⚙️ Technical Requirements

- **Hardware**: Home server or mini-PC with local storage.
- **Software**: Programming languages (Node.js, Python), open-source libraries.
- **Infrastructure**: Task scheduler, persistent storage, backup mechanisms.

---

### 6. 📈 Expected Outcomes

- **Productivity**: Less manual work.
- **Personalization**: Assistants that know the context and adapt.
- **Automation**: Agents that act proactively, not just on request.
