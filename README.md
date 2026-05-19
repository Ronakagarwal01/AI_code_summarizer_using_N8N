<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4b361cb2-f739-4556-8c50-6d717b784999" />



# AI Code Summarizer using n8n

An AI-powered automation workflow built with n8n that automatically reads code from Gmail, generates code comments, creates a simple summary using Google Gemini AI, and sends the final formatted result back through email.

---

## 🚀 Features

- 📧 Reads code directly from Gmail
- 🤖 Uses Google Gemini AI for:
  - Code Summarization
  - Automatic Comment Generation
- ⚡ Parallel execution for faster processing
- 🔀 Merges multiple AI outputs
- 🧾 Converts response into HTML formatted email
- ✉️ Sends final response back to user automatically

---

## 🛠️ Tech Stack

- n8n
- Google Gemini AI
- Gmail API
- HTML Formatting
- AI Automation Workflow

---

## 📌 Workflow Overview

1. Gmail Trigger reads incoming email containing code.
2. Workflow sends code to Gemini AI for:
   - Code Summary
   - Code Comment Generation
3. Both tasks run in parallel.
4. Merge node combines both outputs.
5. Aggregate node structures data properly.
6. HTML formatter creates clean code blocks.
7. Gmail node sends formatted response email.

---

## 🧠 AI Capabilities

### Code Summary
Generates beginner-friendly explanations of code.

### Code Commenting
Adds detailed inline comments without modifying original logic.

### HTML Formatting
Creates professional email-friendly code blocks with syntax highlighting.

---

## 📂 Workflow Nodes Used

- Gmail Trigger
- Google Gemini Chat Model
- Merge Node
- Aggregate Node
- Edit Fields
- HTML Formatter
- Gmail Send Message

---

## 🔄 Workflow Architecture

```text
Gmail Trigger
      │
      ├──► Comment Generator (Gemini AI)
      │
      └──► Code Summarizer (Gemini AI)
                    │
               Merge Outputs
                    │
              Aggregate Data
                    │
              HTML Formatter
                    │
               Send Email
