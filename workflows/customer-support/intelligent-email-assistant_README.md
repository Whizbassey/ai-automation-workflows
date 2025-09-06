# AI Customer Support with Gmail Integration

## Overview
This workflow creates a smart customer support system that automatically handles emails from customers. When someone sends a support email, the AI reads it, looks up information from your product manual and past support cases, then writes a helpful reply. A human approves the response before it gets sent to make sure everything looks good.

---

## What It Does
- **Watches for new support emails** – Checks Gmail every minute for new customer messages  
- **Understands what customers need** – Uses AI to figure out if they need help, want a refund, or have technical questions  
- **Finds the right answers** – Searches through your product manual and old support tickets to get accurate information  
- **Writes professional replies** – Creates helpful responses that sound natural and friendly  
- **Gets human approval** – Sends the draft response to a support agent for review before sending  
- **Handles chat and email** – Works with both Gmail and chat messages  

---

## Key Features
- Smart email classification (technical, billing, sales, returns, general)  
- Automatic response generation using GPT-4  
- Integration with Google Sheets for historical support data  
- PDF manual integration for accurate product information  
- ERP system integration for inventory and pricing  
- Human approval workflow for quality control  
- Multi-channel support (email and chat)  

---

## What You Need Before Starting

### Required Accounts & APIs
- Gmail account with API access  
- OpenAI account with GPT-4 access  
- Google Sheets with your support history  
- Google Drive with your product manual (PDF format)  
- n8n platform account  

### Required Information
- Your support email address  
- Google Sheets document ID with historical support cases  
- PDF manual stored in Google Drive  
- Approver email address for reviewing responses  

---

## Setup Instructions

### Step 1: Connect Your Accounts
**Gmail Connection**  
1. Go to **n8n credentials section**  
2. Add new **Gmail OAuth2 credential**  
3. Follow the authentication steps  

**OpenAI Connection**  
1. Get your **OpenAI API key** from [platform.openai.com](https://platform.openai.com)  
2. Add **OpenAI credential** in n8n  
3. Make sure you have **GPT-4 access**  

**Google Services**  
- Enable **Google Sheets API**  
- Enable **Google Drive API**  
- Use the same Gmail account for consistency  

---

### Step 2: Prepare Your Data
**Create Support History Sheet**  
1. Make a Google Sheet with columns: `Date, Customer, Question, Category, Resolution`  
2. Fill in some past support cases for the AI to learn from  
3. Copy the **sheet ID** from the URL  

**Upload Product Manual**  
1. Upload your product manual as **PDF** to Google Drive  
2. Copy the **file ID** from the sharing URL  

---

### Step 3: Configure the Workflow
**Update Email Settings**  
- Change the approver email from `dummy@mail.com` to your actual email  
- Set up Gmail polling frequency (default: every minute)  

**Update Document References**  
- Replace the **Google Sheets ID** with your support history sheet  
- Replace the **Google Drive file ID** with your product manual  
- Update the **ERP system URL** if you have one  

**Customize Response Template**  
The AI creates responses in this format:  
1. Professional greeting with customer name  
2. `"Thank you for your message."`  
3. Helpful response based on manual and history  
4. Closing with contact information and help resources  
5. `"Have a great day!"`  

---

### Step 4: Test Everything
1. Send a test email to your support address  
2. Check that the AI extracts information correctly  
3. Verify the approval email reaches you  
4. Make sure responses get sent after approval  

---

## Important Notes
- The workflow creates **draft responses** for human review – nothing gets sent automatically  
- Responses are generated in **English** (converted from original German template)  
- The AI only uses information from your **manual and support history**  
- If the AI can’t find good information, it will ask a human to handle the case  
- You can adjust the AI’s response style by editing the prompt  

---

## Troubleshooting
- **No emails detected:** Check Gmail trigger permissions and filters  
- **AI responses seem off:** Review and update the instruction prompt  
- **Approval emails not working:** Verify the approver email address is correct  
- **Manual content not found:** Check Google Drive file permissions and ID  

---

## Customization Ideas
- Add more data sources (CRM, knowledge base)  
- Create different response templates for different product lines  
- Add automatic translation for international customers  
- Set up different approval workflows based on issue severity  
- Add customer satisfaction tracking  
