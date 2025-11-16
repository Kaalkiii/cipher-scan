🛡️ Cipher Scan — Automated Website Security Scanner (n8n Workflow)

Cipher Scan is an automated client-side security auditing workflow built on n8n.
It scrapes any website, analyzes its headers and HTML using AI, grades its security health, and emails a full interactive HTML report.

✨ Features

📥 Form input for entering the website URL

🌐 HTML + HTTP header scraping

🤖 AI-powered Security Configuration Audit

🔍 AI-powered Client-Side Vulnerability Audit

🧮 Automatic Security Grade (A+ → F)

⚠️ Warning & critical issue detection

📜 Beautiful HTML security report

📧 Auto-email delivery via Gmail

📊 Raw headers table + color-coded indicators

🧩 Easy to integrate into DevSecOps workflows

🧠 Workflow Architecture
flowchart TD

A[Form Trigger: Enter URL] --> B[HTTP Request: Scrape HTML & Headers]
B --> C[AI Audit: Security Configuration]
B --> D[AI Audit: Vulnerability Analysis]

C --> E[Merge Audits]
D --> E[Merge Audits]

E --> F[Aggregate Audit Output]
F --> G[Code Processing: Header Analysis + Grading]

G --> H[Generate HTML Report]
H --> I[Send Email via Gmail]

📂 Nodes Used
Node	Purpose
Form Trigger	Accepts user input (Landing Page URL)
HTTP Request	Fetches HTML + response headers
Google Gemini AI (x2)	Performs security & vulnerability audits
Merge Node	Combines audit outputs
Aggregate Node	Normalizes the merged audit
Code Node	Header processing, warning detection, grading
HTML Generator (Code)	Builds full HTML report
Gmail Node	Sends the email
🚀 Setup
1️⃣ Import Workflow

Upload My Workflow 2.json into n8n.

2️⃣ Configure Credentials

You must configure:

Gmail OAuth2

Google Gemini (PaLM) API key

3️⃣ Update Email

In the Gmail node (Send Security Report), replace:

sendTo: you@example.com

4️⃣ Activate the Workflow

Turn it ON → copy the form URL from the Form Trigger.

🖥️ Usage

Open the Cipher Scan form URL

Enter the target website

Submit

Receive a complete audit in your email inbox

📝 The Report Contains

🎯 Overall Security Grade (A+ to F)

🟩🟧🟥 Security header badges

⚠️ Warnings (unsafe inline, missing headers, weak HSTS)

🔴 Critical & high-risk vulnerabilities

🔧 Configuration misconfigurations with recommended fixes

📜 Raw headers table with color-coded rows

📘 Implementation guidance

⏱ Timestamp + target URL metadata

📸 Screenshots (Optional)
/screenshots/cipher-scan-report.png
/screenshots/cipher-scan-workflow.png

🧪 Ideal For

Security engineers

Web developers

DevSecOps pipelines

Automated monitoring

Student cybersecurity labs

⚠️ Disclaimer

Cipher Scan performs non-intrusive, client-side-only checks.
It does not perform penetration testing or server-side exploitation.

Use it ethically.
