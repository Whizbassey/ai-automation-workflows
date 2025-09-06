# Shopify Abandoned Cart Recovery System

## Overview
This smart workflow helps you win back customers who left items in their shopping cart without buying. It waits an hour to see if they come back, then sends a personalized email to encourage them to complete their purchase.

---

## What It Does
- **Finds** customers who abandoned their shopping carts  
- **Waits 1 hour** to see if they complete their purchase  
- **Uses AI** to write personalized recovery emails  
- **Sends emails automatically** to customers who still haven't bought  
- **Keeps track** of all email activity in Google Sheets  

---

## Features
- **Smart Timing** – Waits before sending emails (not too pushy)  
- **AI-Powered Emails** – Creates personal, friendly messages for each customer  
- **Double-Check System** – Only emails people who still haven't purchased  
- **Activity Logging** – Tracks all recovery emails in spreadsheets  
- **Customizable** – Easy to change timing and email content  

---

## How It Works
1. Detects when someone abandons their cart  
2. Waits 1 hour (gives them time to come back)  
3. Checks if they're still abandoned (maybe they bought somewhere else)  
4. AI writes a personal email mentioning their name and items  
5. Sends the email and logs it in Google Sheets  

---

## What You Need Before Starting
- Shopify store with abandoned checkout data  
- **n8n automation platform**  
- **OpenAI API key** (for writing emails)  
- **Gmail account** (for sending emails)  
- **Google Sheets** (for tracking)  

---

## Email Examples
The AI creates emails like:  
- Uses customer's first name  
- Mentions specific items they left behind  
- Friendly, helpful tone (not pushy)  
- May include subtle discount offers  
- Encourages them to complete purchase  

---

## Installation Steps
1. Import the workflow JSON file into **n8n**  
2. Update **Shopify store URLs** in HTTP Request nodes  
3. Add your **Shopify API access token**  
4. Connect your **OpenAI API key**  
5. Set up **Gmail account** for sending emails  
6. Connect **Google Sheets** for logging  
7. Test with a **sample abandoned cart**  

---

## Shopify API Setup
You need to:  
- Get **admin API access** to your Shopify store  
- Replace `"your-store.myshopify.com"` with your actual store URL  
- Replace `"your-access-token"` with your real API token  
- Make sure API has permission to **read checkouts**  

---

## Timing Customization
You can change:  
- **Wait time** (currently 1 hour)  
- **How often** to check for abandoned carts  
- **When to stop trying** (currently stops after customer purchases)  

---

## Tracking and Analytics
The workflow logs:  
- Customer name and email  
- What they abandoned  
- AI-generated email content  
- When emails were sent  
- All saved to **Google Sheets** for analysis  

---

## Best Practices
- Don’t email too quickly (**1 hour minimum**)  
- Keep emails **friendly, not desperate**  
- Mention specific products they wanted  
- Consider offering small discounts  
- Track which emails **work best**  

---

## Safety Features
- Won’t email customers who already completed purchase  
- Prevents **duplicate emails** to same customer  
- Logs all activity for **compliance**  
- Respects **customer privacy**  

---

## Customization Options
You can modify:  
- **Email templates and tone**  
- **Wait times** between checks  
- Which **abandoned carts** to target  
- **Discount offers** in emails  
- **Tracking spreadsheet fields**  

