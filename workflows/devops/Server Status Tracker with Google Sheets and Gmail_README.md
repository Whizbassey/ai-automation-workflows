# Server Monitor with Email Alerts

## Overview
This workflow keeps an eye on your servers by checking if they're running every minute.  
When a server goes down, it automatically sends you an email alert and logs everything to Google Sheets.  

👉 It's like having a security guard for your servers that never sleeps!

---

## What It Does
- ✅ **Checks your servers every minute**  
- 📧 **Sends email alerts when servers go down**  
- 📊 **Tracks server status in Google Sheets**  
- 🕒 **Records timestamps for everything**  
- 🔄 **Runs automatically in the background**

---

## What You Need Before Starting
- [n8n](https://n8n.io) installed and running  
- Google account with Sheets access  
- Gmail account for sending alerts  
- List of server IP addresses to monitor  
- Basic knowledge of n8n workflows  

---

## Setup Instructions

### Step 1: Prepare Your Google Sheet
1. Create a new Google Sheet called **`Server-Monitor`**  
2. Add three tabs:  
   - `Server_List` → Put your server IPs here  
   - `Server_Status_Alive` → For healthy servers  
   - `Server_Status_Down` → For problem servers  

---

### Step 2: Import the Workflow
1. Copy the **JSON file** content  
2. Go to **n8n** → click **Import from File**  
3. Paste the JSON and **save**  

---

### Step 3: Connect Your Accounts
- Set up **Google Sheets** connection  
- Connect your **Gmail** account  
- Update the **Sheet ID** in the workflow  

---

### Step 4: Add Your Servers
1. Open your Google Sheet  
2. In the `Server_List` tab, add your server addresses  
3. Put **one server per row** in the `Server` column  

---

### Step 5: Test and Activate
- Test the workflow manually first  
- Check if **emails work properly**  
- Activate the workflow when ready  

---

## How It Works
- The workflow runs **every minute** and checks each server in your list.  
- If a server responds, it marks it as **Alive** in the sheet.  
- If it doesn't respond, it sends an **email alert** and logs it as **Down**.  

👉 Simple as that!

---

## Troubleshooting
- ✅ Make sure your server URLs start with `http://`  
- ✅ Check your **Google Sheets permissions**  
- ✅ Verify your **Gmail credentials** are working  
- ✅ Test with **one server first** before adding many  
