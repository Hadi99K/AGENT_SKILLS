# 🤖 AGENT_SKILLS

> A collection of plug-and-play AI agent skills for project coordination, phase management, and multi-agent synchronization.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Compatibility: opencode](https://img.shields.io/badge/Compatibility-opencode-blue.svg)]()

---

## 📖 Introduction

**AGENT_SKILLS** is an open-source repository of reusable AI agent skills designed to help developers manage structured, multi-agent workflows directly inside their codebases.

Whether you are starting a brand-new project or wrapping up a development phase, these skills give your AI agents clear, repeatable instructions to keep your work organized and your team (human or AI) in sync.

---

## 🛠️ Available Skills

### 1. `init-agent-sync`

**Description:** Initializes the `AGENT_SYNC.md` coordination hub for AI agent task tracking and multi-agent handoffs.

**What it does:**
- Creates an `AGENT_SYNC.md` file in the root of your project (if one doesn't already exist).
- Populates it with standard AI agent instructions, a context/state section, a session task board, and a handoff log.
- Sets up the foundation for multi-agent workflows so AI assistants can cleanly pass tasks to one another.

**When to use it:**  
Run this skill when starting a new project, or when you want to introduce the AI agent synchronization system to an existing repository.

---

### 2. `wrap-phase`

**Description:** Wraps up a development phase by summarizing work, cleaning the `AGENT_SYNC.md` file, and committing the result.

**What it does:**
- Reads `AGENT_SYNC.md` to understand completed work.
- Adds a Phase Summary highlighting everything built and key technical decisions.
- Cleans the Handoff Log (keeps only the most recent entry) and clears completed tasks from the task board.
- Updates the Current Phase status to reflect completion.
- Automatically stages, commits, and pushes `AGENT_SYNC.md`.

**When to use it:**  
Use this skill when you or your AI agent is asked to *"wrap up the phase"*, *"wrap the phase"*, or *"clean up AGENT_SYNC"*.

---

## 🚀 Getting Started

### Prerequisites

- [Git](https://git-scm.com/) installed on your machine.
- A GitHub account.
- An AI coding assistant that supports agent skills (e.g., [opencode](https://opencode.ai/)).

### Clone the Repository

Open your terminal or command prompt and run:

```bash
git clone https://github.com/Hadi99K/AGENT_SKILLS.git
cd AGENT_SKILLS
```

---

## 💡 Usage

Each skill lives in its own folder and is defined by a `SKILL.md` file. Load the skill into your AI agent by pointing it at the relevant `SKILL.md`, or by copying its contents into your agent's skill/instruction configuration.

### 📂 Where Are Skills Stored?

Skills are loaded by your AI coding assistant from one of two locations:

| Scope | Path |
|---|---|
| **Project (local)** | `.opencode/skills/<name>/SKILL.md` inside your project folder |
| **Global (all projects)** | `~/.config/opencode/skills/<name>/SKILL.md` on your computer |

- Use the **Project config** path when you want a skill available only for a specific repository.
- Use the **Global config** path when you want a skill available across all your projects.

> **Example – adding `init-agent-sync` to a project:**
> ```bash
> mkdir -p .opencode/skills/init-agent-sync
> cp init-agent-sync/SKILL.md .opencode/skills/init-agent-sync/SKILL.md
> ```

### ▶️ Running a Skill

Once a skill is placed in one of the locations above, you can run it directly from your AI assistant:

1. Type the `/skills` command in your AI assistant's chat or terminal.
2. A list of all your saved skills will appear.
3. Select the skill you want to run from the list.

> **Tip:** If you don't see a skill listed, double-check that its `SKILL.md` file is saved in one of the two paths shown in the table above.

### Using `init-agent-sync`

```bash
# Navigate to the skill folder
cd init-agent-sync

# Open SKILL.md to read the full instructions for your agent
cat SKILL.md
```

**Invoke the skill** by telling your AI agent:
> *"Run the init-agent-sync skill."*

The agent will check for an existing `AGENT_SYNC.md` and either create a new one or ask before overwriting.

---

### Using `wrap-phase`

```bash
# Navigate to the skill folder
cd wrap-phase

# Open SKILL.md to read the full instructions for your agent
cat SKILL.md
```

**Invoke the skill** by telling your AI agent:
> *"Wrap up the phase."* or *"Clean up AGENT_SYNC."*

The agent will summarize accomplishments, clean old log entries, update the phase status, and push the changes automatically.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/your-skill-name`
3. Add your skill in a new folder with a `SKILL.md` file following the existing format.
4. Commit your changes: `git commit -m "feat: add your-skill-name skill"`
5. Push to your branch: `git push origin feature/your-skill-name`
6. Open a Pull Request.

Please check the [issues page](https://github.com/Hadi99K/AGENT_SKILLS/issues) before submitting a new request.

---

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
