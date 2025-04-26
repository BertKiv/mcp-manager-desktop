# 🤖 GitHub Copilot Instructions for VSCode

These are strict operational and stylistic guidelines Copilot must follow during code analysis, suggestions, and implementation in this project.

## ⚙️ General Workflow
1. **ANALYZE** the code and determine potential improvements.
2. **STORE** findings in memory/context.
3. **WAIT** for next explicit instructions.
4. **DO NOT** perform any changes yet.
5. **COMMUNICATE IN POLISH** in this chat.
6. **WRITE CODE IN ENGLISH**, including all code comments.
7. **UPDATE DOCUMENTATION** in English under `docs/` if functionality is added or changed.
8. **LOG ALL APPROVED CHANGES** in `CHANGES.md` or `CHANGELOG.md` located in the project root, next to `README.md`.
9. **MAINTAIN AND UPDATE `TODO.md`** in the project root with all relevant technical debts, suggestions, or upcoming improvements.

## 🧾 Documentation Rule
- After implementing **approved** code changes, **append** a clear, concise summary of the modification to `CHANGES.md` or `CHANGELOG.md` (use whichever is present). If neither exists, **create `CHANGES.md`**.
- Each entry should follow this format:
  ```
  ## [YYYY-MM-DD]
  - [Short description of the change] ([filename or module])
  ```

## 📋 TODO Management
- As part of your analysis or implementation, identify any **technical debt**, **deferred improvements**, or **pending tasks**.
- Add them to `TODO.md` using the following structure:
  ```
  - [ ] [Short description of task] ([context/file])
        ⤷ Notes: [Optional elaboration, reasoning, or references]
  ```
- If a task is completed, mark it as:
  ```
  - [x] [Task completed] ([context/file])
  ```

## 🧩 Critical Development Guidelines
- ✅ **Preserve** all existing business logic unless explicitly instructed otherwise.
- 🛑 **Do NOT delete** or refactor production code without approval.
- 🔍 **Report** any structural or architectural concerns before making changes.
- 🧠 Always apply **DRY** (Don't Repeat Yourself) and **KISS** (Keep It Simple, Stupid) principles.
- ⚠️ Avoid "spaghetti code" and keep functions modular and readable.
- 🕐 Allow operations to **fully complete** before interrupting (no premature `ctrl+c`).

## 🛠️ Change Implementation Protocol
1. **Analysis** – Identify the exact problem or opportunity.
2. **Consultation** – Propose a solution or refactor plan.
3. **Authorization** – Wait for explicit go-ahead.
4. **Implementation** – Apply only the approved changes.
5. **Documentation** – Update `docs/`, `CHANGES.md`, and `TODO.md` accordingly.

## 🚫 Enforcement
- All code edits must be **additive by default**.
- Code related to models or core infrastructure is **strictly protected**.
- File system modifications are limited to the **current working directory** unless instructed otherwise.
- 🧭 When in doubt – **ask first**.