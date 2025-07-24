# 🤖 AI Automated Hiring Workflow with n8n

This is a fully automated recruitment pipeline powered by [n8n](https://n8n.io), OpenAI, Google Sheets, and Gmail. It parses job applications directly from email (e.g., Indeed), extracts relevant candidate data, and manages their progression from application to hiring—all without human intervention.

---

## 💼 What It Does

1. **Email Parsing**  
   - Listens for incoming job applications via Gmail (Indeed subject lines).
   - Uses OpenAI (GPT-4o-mini) to extract job titles from subject text.

2. **Candidate Database (Google Sheets)**  
   - Automatically logs first name, last name, job title, email, and more.
   - Generates a unique candidate code for tracking.

3. **Automated Emails**  
   - Sends onboarding forms via Gmail.
   - Includes code-based access validation.

4. **Form Integration & Test Handling**  
   - Processes onboarding form data and updates sheet.
   - Sends test instructions, collects Google Drive links.
   - Approves/rejects based on experience or test score.

5. **Interview Booking & Final Steps**  
   - Triggers Cal.com to book interviews.
   - Marks final status like “Interview Scheduled”, “Hired”, etc.

---

## 🚀 Why Use This?

Recruiting manually is tedious. This agent allows you to:

- Eliminate repetitive hiring tasks
- Auto-respond to applicants based on form submissions
- Keep everything tracked in Google Sheets
- Use AI to parse unstructured data like subject lines
- Improve speed & accuracy in screening talent

---

## 🔧 APIs & Services Used

| Service         | Purpose                            |
|----------------|------------------------------------|
| Gmail API       | Email fetch & send automation      |
| OpenAI (GPT-4o) | Extract job title from subject     |
| Google Sheets API | Candidate tracking                |
| n8n             | Workflow automation engine         |
| Cal.com API     | Interview scheduling               |
| Slack (optional)| Notifications (currently disabled) |

---

## 🛠️ Setup Instructions

1. **Clone this Repo**  
   Download or clone the workflow and import into your [n8n instance](https://docs.n8n.io/hosting/installation/).

2. **Configure Credentials**
   - Gmail (OAuth2)
   - OpenAI API Key (GPT-4o or GPT-3.5)
   - Google Sheets Access (OAuth2)
   - (Optional) Slack Bot Token
   - Cal.com API Token

3. **Update Workflow**  
   - Replace placeholder emails and sheet IDs with your own.
   - Link to your onboarding & test forms.
   - Customize rejection logic (e.g., experience threshold).

4. **Activate Webhooks & Triggers**  
   Ensure form triggers and calendar integrations are active.

---

## 📌 Developed By

**Tufaque Sayyed**  
AI/ML Engineer | Data Scientist | Ai Agent Builder 

🌐 [Portfolio](https://tufaquesayyed.vercel.app)  
🔗 [LinkedIn](https://www.linkedin.com/in/tufaque-sayyed-843596364/)

---

> ⚙️ This project demonstrates the power of AI + n8n in building robust, scalable automation solutions in the recruitment space.
