# B2B Lead Qualifier & Outreach System

## Overview
This smart workflow takes leads from your contact forms and automatically decides if they're worth your time. For the good leads, it sends them a professional email and saves their info to Google Sheets. No more manually checking every single lead!

---

## What It Does
- **Gets lead information from contact forms**  
- **Uses Apollo API** to find more details about the person  
- **AI lead scoring (1-10 scale)** to determine quality  
- **Contacts only high-scoring leads** (6 or above)  
- **Sends personalized outreach emails automatically**  
- **Saves everything to Google Sheets** for tracking  

---

## Features
- **Smart Lead Scoring**: AI checks if they're in AI/tech industry and have decision-making roles  
- **Automatic Outreach**: Sends professional emails to qualified leads only  
- **Data Enrichment**: Finds job titles, company info, and more using Apollo  
- **Contact Form Integration**: Works with your existing forms  
- **CRM Integration**: Saves lead data to Google Sheets  

---

## What You Need Before Starting
- **n8n automation platform**  
- **OpenAI API key** (for AI scoring)  
- **Apollo.io API access** (for lead data)  
- **Gmail account** (for sending emails)  
- **Google Sheets** (for storing leads)  

---

## How the Scoring Works
The AI gives leads points based on:

### Industry Match (up to 5 points)
- **5 points**: AI, Machine Learning, Data Science companies  
- **3–4 points**: Related fields like analytics, automation  
- **0–2 points**: Unrelated industries  

### Job Title Match (up to 5 points)
- **5 points**: Decision makers (CTO, AI Director, Head of AI)  
- **3–4 points**: Mid-level AI professionals (ML Engineer, Data Scientist)  
- **0–2 points**: Junior roles or unrelated positions  

➡️ Only leads scoring **6+** get contacted automatically.  

---

## Installation Steps
1. Import the **workflow JSON file** into n8n  
2. Set up your **contact form** (or use the included form trigger)  
3. Add your **API credentials**:  
   - OpenAI API key  
   - Apollo.io API key  
   - Gmail account connection  
   - Google Sheets access  
4. Update the **email template** with your company details  
5. Test with **sample lead data**  

---

## Form Fields Needed
Your contact form should collect:  
- **Full Name**  
- **Email Address**  
- **Phone Number**  
- **LinkedIn Profile URL** (optional)  

---

## Email Customization
The workflow sends emails like this:  
- Professional subject line  
- Mentions their **company name**  
- Suggests a **quick call**  
- Includes your **contact details**  

👉 You can customize the email template in the **AI Agent node**.  




