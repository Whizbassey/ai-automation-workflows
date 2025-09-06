# QuickBooks Customer & Estimate Creation from Google Sheets

## Overview
This workflow automatically creates new customers and estimates in QuickBooks whenever someone adds a new row to your Google Sheet. It saves tons of time by removing manual data entry and makes sure nothing gets missed. Perfect for sales teams who want to speed up their quote process!

---

## What It Does
- 📊 **Watches your Google Sheet** for new customer data  
- 🔍 **Checks** if the customer already exists in QuickBooks  
- 👤 **Creates new customers** automatically if they don't exist  
- 💰 **Generates estimates** based on the amount in your sheet  
- ⚡ **Works instantly** when new data is added  
- 🔄 **Prevents duplicates** from being created  

---

## What You Need Before Starting
- **N8N** installed and running  
- **QuickBooks Online** account  
- **Google account** with Sheets access  
- **QuickBooks OAuth2** credentials  
- **Google OAuth2** credentials  
- A **Google Sheet** with customer information  

---

## Setup Instructions

### Step 1: Create Your Google Sheet
1. Make a new Google Sheet for customer data  
2. Add these columns (**exact names matter**):  
   - **CustomerName** – Full name of the customer  
   - **Email** – Customer's email address  
   - **Phone** – Customer's phone number  
   - **Company Name** – Name of their business  
   - **Amount** – Estimate amount in numbers  

---

### Step 2: Get QuickBooks API Access
1. Go to **QuickBooks Developer Dashboard**  
2. Create a new **app** for your business  
3. Get your **OAuth2 credentials**  
4. Make sure you have **Accounting scope** enabled  
5. Test the connection in **N8N**  

---

### Step 3: Setup Google Sheets Connection
1. In N8N, create **Google OAuth2 credentials**  
2. Enable both **Google Sheets** and **Google Drive**  
3. Test the connection with your sheet  
4. Make sure N8N can read your data  

---

### Step 4: Import and Configure Workflow
1. Copy the **JSON workflow content**  
2. Import it into **N8N**  
3. Replace `{YOUR_GOOGLE_SHEETS_ID}` with your actual **Sheet ID**  
4. Connect your **QuickBooks and Google credentials**  
5. Update the **Item ID** in the estimate creation (default: `"15"`)  

---

### Step 5: Test the Workflow
1. Add a **test row** to your Google Sheet  
2. Fill in all the required fields  
3. Wait about 1 minute for the trigger  
4. Check QuickBooks for the new customer and estimate  
5. Verify everything looks correct  

---

### Step 6: Go Live
1. Train your team on the **sheet format**  
2. Activate the workflow in **N8N**  
3. Monitor the first few entries  
4. Set up **error notifications** if needed  

---

## How It Works

### The Process Flow
1. **New Row Added** – Someone adds customer data to your Google Sheet  
2. **Data Check** – Workflow grabs the information and cleans it up  
3. **Customer Search** – Looks for existing customer with the same name in QuickBooks  
4. **Decision Point** – If customer exists, skip creation; if not, create new customer  
5. **Estimate Creation** – Makes a new estimate for the customer with the specified amount  
6. **Complete** – Everything is ready in QuickBooks for your team  

---

### Important Details
- The workflow checks **every minute** for new rows  
- Customer names must **match exactly** to avoid duplicates  
- Estimates use a **default item** (ID `"15"`) – change this to match your products  
- All fields in the sheet are **required** for the workflow to work  

---

## Customization Options
- Change the **estimate line items** and descriptions  
- Add more customer fields (e.g., **address**, **company size**)  
- Include **tax calculations** in estimates  
- Send **email notifications** when estimates are created  
- Connect to other tools like **CRM systems**  

---

## Common Issues and Solutions
- **Customer not created** → Check if all required fields have data  
- **Estimate fails** → Make sure the **Item ID** exists in QuickBooks  
- **Duplicates created** → Customer names must match exactly (case-sensitive)  
- **Connection errors** → Refresh your **OAuth2 tokens**  
- **Sheet not triggering** → Verify the **Sheet ID** is correct  

---

## Best Practices
- Keep **customer names consistent** in your sheet  
- Don’t leave any **required fields empty**  
- Test with **small amounts first**  
- Train team members on **exact field names**  
- Monitor QuickBooks for **accuracy**  
- Set up **backup procedures**  

---

## Security Notes
- Keep your **API credentials secure**  
- Don’t share sheet access with unauthorized people  
- Use **strong passwords** for all accounts  
- Regularly review **QuickBooks permissions**  
- Monitor for **unusual activity**  
