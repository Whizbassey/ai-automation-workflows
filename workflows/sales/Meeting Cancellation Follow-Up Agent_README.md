# Auto Follow-Up for Canceled Calendly Meetings with GPT-4, Loom & Asana

## 🚀 Overview
This workflow automatically sends **friendly follow-up emails** when someone cancels a meeting on your **Calendly**.  

Instead of losing that lead forever, it sends a personalized message (with your Loom video) and creates a task in **Asana** for manual follow-up.  
👉 It turns canceled meetings into **new opportunities** for your sales pipeline.

---

## ✅ What It Does
- 📅 Detects when someone cancels a Calendly meeting  
- 🤖 Uses GPT-4 to generate **friendly follow-up emails**  
- 🎥 Includes your **pre-recorded Loom video**  
- 📧 Sends emails automatically via **Gmail**  
- 📝 Creates tasks in **Asana** for manual follow-up  
- 💼 Keeps your sales pipeline active and organized  

---

## 🛠 What You Need Before Starting
- [n8n](https://n8n.io) installed and running  
- **Calendly** account with webhook access  
- **OpenAI API key** (for GPT-4)  
- **Gmail** account for sending emails  
- **Asana** account for task management  
- A **Loom video** explaining your service  

---

## ⚙️ Setup Instructions

### Step 1: Record Your Loom Video
1. Go to [Loom](https://loom.com) and create an account  
2. Record a **short 3–5 min video** covering:  
   - What you would have discussed in the meeting  
   - Key benefits of your service  
   - How to get in touch when they’re ready  
3. Make the video **public** and copy the link  

---

### Step 2: Get Your API Keys
1. **OpenAI (GPT-4):**  
   - Go to [platform.openai.com](https://platform.openai.com)  
   - Create an account and get API access  
   - Save your API key  

2. **Calendly Webhook Setup:**  
   - Log into your Calendly account  
   - Go to **Integrations & Apps**  
   - Set up a webhook for **`invitee.canceled`** events  

---

### Step 3: Setup Asana Integration
1. Create an **Asana account** (if not already)  
2. Create a project called **Follow-up Tasks**  
3. Get your **Workspace** and **Project IDs**  
4. In n8n, add an **Asana OAuth2 credential**  

---

### Step 4: Import & Configure the Workflow
1. Import the provided JSON file into n8n  
2. Connect your Gmail account  
3. Add your OpenAI API key  
4. Paste your Loom video link into the workflow  
5. Configure Asana **Workspace & Project IDs**  
6. Test all connections  

---

### Step 5: Connect to Calendly
1. Point the Calendly webhook to your **n8n instance**  
2. Cancel a test meeting to trigger the workflow  
3. Verify:  
   - Email is sent  
   - Task is created in Asana  
4. Activate the workflow  

---

### Step 6: Customize Your Messages
1. Edit the **GPT-4 prompt** to match your brand tone  
2. Update the **email subject line**  
3. Customize the **Asana task template**  
4. Experiment with different styles  

---

## 🔄 How It Works

### When Someone Cancels
1. **Calendly webhook** triggers the n8n workflow  
2. Workflow extracts **name, email, reason for cancel**  
3. **GPT-4** generates a short, friendly follow-up message  
4. Loom video link is added to the email  
5. **Email is sent** automatically through Gmail  
6. **Asana task** is created for manual follow-up  

---

## 📧 Example Emails
The AI generates messages like:  
- “No worries about the cancellation!”  
- “I recorded a quick video covering what we would have discussed”  
- “Feel free to reach out when the timing works better”  

---

## 💡 Best Practices
- Keep emails **short, warm, and non-pushy**  
- Deliver real value in your **Loom video**  
- Add a **rebooking link** if possible  
- Follow up manually after a few days  
- Track **which videos get watched**  

---

## 🎨 Customization Ideas
- Different Loom videos for different meeting types  
- Add **calendar rebooking links** in follow-ups  
- Create **multi-step follow-up sequences**  
- Track **email open & click rates**  
- Sync with your **CRM**  

---

## 🐞 Troubleshooting
- ❌ **No emails sent** → Check Gmail connection  
- ❌ **Webhook not triggering** → Verify Calendly webhook URL  
- ❌ **Generic AI messages** → Improve GPT prompt  
- ❌ **Asana tasks not created** → Check workspace/project IDs  
- ❌ **Loom video not showing** → Ensure video is **public**  

---

## 🎯 Success Tips
- Test the workflow with your own cancellations first  
- Make your Loom video **genuinely helpful**  
- Keep follow-up **human, not spammy**  
- Respond quickly when people reply  
- Update videos based on **client feedback**  

---

## 🔒 Privacy Notes
- Only email people who **booked with you**  
- Follow **email marketing laws** (CAN-SPAM, GDPR)  
- Allow opt-out of follow-ups  
- Never share client data publicly  
- Respect cancellation reasons  
