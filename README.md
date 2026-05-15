# ai-tender-automation-n8n
AI-Powered Construction Tender Automation (n8n & LLM)
This project is a modular automation engine designed to solve the problem of unstructured data in the construction industry. It automatically extracts tender details (Project Name, Budget, Location) from conversational inputs and logs them into a structured "Universal Memory" database (Google Sheets).

🚀 Overview
Construction teams often receive project information through unstructured channels (chats, emails, notes). This workflow automates the transition from unstructured communication to structured business intelligence using high-speed AI inference.

🛠 Tech Stack
Orchestration: n8n (Self-hosted)

AI Reasoning: Groq Cloud (Llama 3.3 70B Model)

Integration: Google Sheets API (via OAuth2)

Data Transformation: Custom JavaScript / JSON Parsing

🧠 Key Features
Zero-Latency Extraction: Utilizes Groq’s LPU inference engine for near-instant data processing.

Deterministic Output: Uses prompt engineering to force the LLM to output valid JSON.

Data Integrity: Implemented a JSON.parse() transformation layer in n8n to ensure that only specific data points are mapped to the correct database columns.

Scalable Architecture: Built with a modular approach, allowing for easy replacement of the trigger (e.g., Slack, Gmail) or the storage (e.g., PostgreSQL, Salesforce).

📽️ Demo
https://drive.google.com/file/d/1hQRwPUr_fB-HdcCE2vzHc1PhO6KYaU2g/view?usp=drive_link
📂 How to use
Import the workflow.json file into your n8n instance.

Configure your Google Sheets Credentials via OAuth2.

Set up your Groq API Key in the AI Agent node.

Run the workflow and start chatting with the agent!
