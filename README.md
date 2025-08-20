# 📧 Gmail Automation with n8n

This repository contains an **n8n workflow** that automatically classifies incoming Gmail messages into categories and generates a polite, HTML-formatted draft reply. The workflow helps save time by preparing responses while leaving the final review and sending decision to the user.

---
<img width="1498" height="761" alt="image" src="https://github.com/user-attachments/assets/584747a5-1167-44b0-83e0-3955b3ec3e32" />

<img width="1350" height="668" alt="image" src="https://github.com/user-attachments/assets/0da2835a-831f-494d-b9ad-446ab8a9a543" />


## ⚙️ Workflow Overview

The automation performs the following steps:

1. **Gmail Trigger** – Listens for new incoming emails.
2. **Get a Message** – Fetches the subject and body of the new email.
3. **AI Agent (OpenAI Chat Model)** –  
   - Classifies the email into one of the categories:  
     - `course`  
     - `Doubts`  
     - `sponsorship`  
   - Generates a respectful, professional **HTML reply draft**.
4. **Structured Output Parser** – Ensures the AI response is in a valid JSON format (`label` + `reply`).
5. **Get Many Labels in Gmail** – Retrieves existing Gmail labels.
6. **Add Label to Message** – Applies the classification label to the email in Gmail.
7. **Create a Draft** – Creates an HTML reply draft in Gmail that the user can review and send.

---

## 🖼️ Workflow Screenshot

![Workflow Screenshot](./workflows/screenshot.png)

---

## 📂 Repository Structure

