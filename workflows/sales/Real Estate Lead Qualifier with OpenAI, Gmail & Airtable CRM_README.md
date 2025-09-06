# Real Estate Lead Qualifier

## Overview
This workflow helps real estate agents automatically sort good leads from time-wasters. When someone fills out your property form, it uses AI to check if they're serious buyers, then sends alerts for the best leads and saves everything to your CRM.

---

## What It Does
- **Gets property inquiries** from your website forms  
- **Uses AI to score leads** from 0–100 based on their budget, timeline, and location  
- **Sends email alerts** automatically for high-scoring leads (70+ points)  
- **Saves all lead information** to Airtable CRM  
- **Organizes data** so you can follow up easily  

---

## Features
- **Smart Lead Scoring**: AI analyzes budget, urgency, and location preferences  
- **Instant Notifications**: Get emailed immediately about qualified leads  
- **CRM Integration**: All leads saved to Airtable with scores and details  
- **Custom Forms**: Easy-to-use property inquiry forms  
- **No Manual Work**: Everything happens automatically  

---

## How the Scoring Works
The AI gives points based on:

### **Budget Analysis**
- Higher budgets = more points  
- AI converts budget ranges to actual numbers  

### **Timeline Urgency**
- **ASAP / This month** → High urgency  
- **6–12 months** → Medium urgency  
- **Just looking** → Low urgency  

### **Location Preference**
- **Sydney** gets bonus points (customizable)  
- Other locations = standard scoring  

### **Qualification Threshold**
- **70+ points** → Qualified lead (triggers email alert)  
- **Under 70** → Still saved to CRM but no alert  

---

## What You Need Before Starting
- **n8n automation platform**  
- **OpenAI API key**  
- **Gmail account** for notifications  
- **Airtable account** for CRM  
- **Website** to host the property form  

---

## Form Fields Collected
The property inquiry form asks for:  
- Full Name  
- Email Address  
- Budget Range (e.g., `$500K–$800K`)  
- Preferred Location  
- Purchase Timeline (e.g., `Next 3 months`)  
- Property Type (house, apartment, etc.)  

---

## Installation Steps
1. Import the workflow JSON file into **n8n**  
2. Connect your accounts:  
   - OpenAI API key  
   - Gmail account  
   - Airtable base and table  
3. Customize the form fields if needed  
4. Set your **email address** for notifications  
5. Test with sample lead data  
6. Add the form to your website  

---

## Airtable Setup
The workflow creates records with these fields:  
- Name and Email  
- Budget and Location  
- Timeline and Lead Score  
- All organized for **easy follow-up**  

---

## Email Notifications
When a **qualified lead** (70+ points) is detected, you’ll receive an email with:  
- Lead’s name and contact info  
- Their budget and location preferences  
- Timeline for purchasing  
- AI confidence score  

---

## Customization Options
You can easily change:  
- **Scoring criteria** (budget thresholds, location preferences)  
- **Qualification threshold** (default: 70 points)  
- **Email template** and recipient  
- **Form fields** and styling  
- **CRM fields** and organization  
