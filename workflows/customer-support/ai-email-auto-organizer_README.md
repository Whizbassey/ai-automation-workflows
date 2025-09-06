# ai-email-auto-organizer

## Overview
This workflow automatically reads your emails and sorts them into helpful categories using AI. Instead of manually organizing hundreds of emails, the AI looks at each message and puts the right label on it. It runs every few minutes and only processes emails that haven't been sorted yet.

---

## What It Does
- **Reads your emails automatically** – Checks Gmail for messages that need sorting  
- **Understands what each email is about** – AI reads the subject and content  
- **Adds the right labels** – Puts emails in categories like Newsletter, Invoice, Urgent, etc.  
- **Creates new labels when needed** – If a category doesn't exist, it makes one  
- **Skips emails already sorted** – Won’t process emails that already have labels  
- **Runs on schedule** – Checks for new emails every 2 minutes  

---

## Available Email Categories
The AI can sort emails into these **17 categories**:

### Work & Business
- **Invoice** – Bills, payment requests, receipts  
- **Proposal** – Business offers, contracts, collaboration requests  
- **Action Required** – Things you need to do (book, confirm, complete)  
- **Task** – To-do items and project steps  
- **Follow-up Reminder** – Reminders about pending items  

### Communication
- **Inquiry** – Questions that need your reply  
- **Personal** – Messages from friends and family  
- **Urgent** – Time-sensitive or emergency emails  

### Updates & Notifications
- **Newsletter** – Subscription updates, promotions, digests  
- **System Notification** – Alerts from monitoring tools, cloud services  
- **Social/Networking** – Notifications from GitHub, forums, social sites  
- **Job Update** – Messages from recruiters or job portals  

### Financial
- **Bank** – Bank statements, transaction alerts, fraud warnings  
- **Receipt** – Purchase confirmations, tickets, order receipts  
- **Subscription Renewal** – Software licenses, membership renewals  

### Events & Spam
- **Event Invite** – Calendar invitations and RSVPs  
- **Spam/Junk** – Unwanted bulk mail and obvious ads  

---

## What You Need Before Starting

### Required Accounts
- Gmail account with API access  
- OpenAI account for AI processing  
- n8n platform account  

### Gmail Setup
1. Enable **Gmail API** in Google Cloud Console  
2. Create **OAuth2 credentials** for n8n  
3. Make sure n8n can read and modify your Gmail  

---

## Setup Instructions

### Step 1: Connect Gmail
**Get Gmail Credentials**
1. Go to Google Cloud Console  
2. Enable Gmail API  
3. Create OAuth2 credentials  
4. Download the credentials file  

**Add to n8n**
1. Go to **n8n credentials section**  
2. Add new **Gmail OAuth2 credential**  
3. Upload your credentials file  
4. Complete the authentication process  

---

### Step 2: Connect OpenAI
**Get OpenAI API Key**
1. Sign up at [platform.openai.com](https://platform.openai.com)  
2. Go to **API Keys** section  
3. Create a new API key  
4. Copy the key (**you won’t see it again**)  

**Add to n8n**
1. Add **OpenAI credential** in n8n  
2. Paste your API key  
3. Test the connection  

---

### Step 3: Customize Categories (Optional)
You can change the email categories by editing the AI prompt:  
- Open the **"Categorize Email with AI"** node  
- Find the system message with label definitions  
- Add, remove, or modify categories as needed  
- Update the label list to match your changes  

---

### Step 4: Adjust Excluded Labels
The workflow skips emails that already have certain labels. To change this:  
1. Open the **"Filter Emails Without Excluded Labels"** node  
2. Look at the excluded label IDs list  
3. Add or remove label IDs based on your Gmail setup  
4. Save the changes  

---

### Step 5: Set Schedule
The workflow runs every **2 minutes** by default:  
- Click on **"Schedule Trigger"** node  
- Change the interval if you want (every minute, every 5 minutes, etc.)  
- You can also set it to run only during work hours  

---

### Step 6: Test It Out
1. Run the workflow manually first  
2. Check if it processes a few emails correctly  
3. Look at the labels it creates  
4. Make sure the categories make sense  
5. Let it run automatically once you’re happy  

---

## How It Works

### Processing Steps
1. **Get Recent Emails** – Fetches last 20 emails from Gmail  
2. **Filter Already Processed** – Skips emails that already have organization labels  
3. **Process Each Email** – Loops through unprocessed emails one by one  
4. **Extract Email Content** – Gets sender, subject, and body text  
5. **AI Categorization** – AI reads content and picks the best category  
6. **Check for Existing Label** – Looks for a Gmail label matching the category  
7. **Create or Apply Label** – Makes new label if needed, then applies it to email  
8. **Move to Next Email** – Continues until all emails are processed  

### Smart Features
- **Prevents Double Processing** – Won’t re-categorize emails that already have labels  
- **Handles New Categories** – Creates Gmail labels automatically when needed  
- **Batch Processing** – Handles multiple emails efficiently  
- **Error Handling** – Continues working even if one email causes problems  

---

## Important Notes
- The AI only reads email content to **categorize it** – nothing gets deleted or moved  
- New Gmail labels are created automatically when the AI suggests new categories  
- The workflow only processes emails that don’t already have organizational labels  
- The schedule can be adjusted based on your email volume  
- OpenAI API calls cost money, but categorization is **very cheap (pennies per email)**  

---

## Troubleshooting
- **No emails getting processed:** Check Gmail API permissions  
- **Wrong categories:** Review and adjust the AI prompt with better examples  
- **Labels not applying:** Verify Gmail API can modify labels  
- **Too many API calls:** Reduce the schedule frequency or email batch size  
- **Missing credentials:** Make sure both Gmail and OpenAI credentials are working  

---

## Customization Ideas
- Add categories specific to your work (like **Client Projects** or **Marketing**)  
- Set up different rules for different email addresses  
- Add automatic forwarding for urgent emails  
- Create follow-up reminders for action-required emails  
- Integrate with task management tools for action items  
