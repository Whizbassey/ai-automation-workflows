# AI-Powered Lead Research & Personalized Email Generation

## 🚀 Overview
This powerful workflow automatically researches companies, learns about their business, and creates **personalized sales emails** using AI.  
It’s like having a smart sales assistant that never sleeps!  

The system finds the perfect things to say to each potential customer—helping you start meaningful conversations that convert.

---

## ✅ What It Does
- 🔍 Automatically researches companies online  
- 🧠 Uses AI to understand their business needs  
- 📧 Creates personalized sales emails  
- 📊 Tracks everything in Google Sheets  
- 🎯 Finds the best approach for each lead  
- 🔗 Creates clickable email sending links  

---

## 🛠 What You Need Before Starting
- [n8n](https://n8n.io) installed and running  
- Google account with **Sheets** access  
- **OpenAI API key** (for GPT-4)  
- **Tavily API key** (for internet research)  
- Gmail account for sending emails  
- A list of companies to contact  

---

## ⚙️ Setup Instructions

### Step 1: Get Your API Keys
1. **OpenAI API Key**  
   - Go to [platform.openai.com](https://platform.openai.com)  
   - Create an account and get API access  
   - Save your API key safely  

2. **Tavily API Key**  
   - Visit [tavily.com](https://tavily.com)  
   - Sign up for their search service  
   - Get your API key for internet research  

---

### Step 2: Create Your Google Sheet
1. Make a new sheet called **`Leads To Sales`**  
2. Create these tabs:  
   - **Leads** → Main data with company info  
   - **Template** → Email templates for different stages  
   - **List Product** → Your services and products  

3. In the **Leads** tab, add these columns:  
   - `Nama` (Name)  
   - `Jabatan` (Position)  
   - `Email`  
   - `Perusahaan` (Company)  
   - `Hasil Riset` (Research Results)  
   - `Status`  
   - `Send Email Perkenalan` (Introduction Email)  

---

### Step 3: Import and Connect Everything
1. Import the JSON workflow into **n8n**  
2. Connect your **Google Sheets** account  
3. Add your **OpenAI API key**  
4. Add your **Tavily API key**  
5. Update all **Sheet IDs** to match yours  

---

### Step 4: Fill Your Templates
1. Go to the **Template** tab in your sheet  
2. Add different **email themes** for each sales stage  
3. Include **sample messages** that AI can learn from  
4. Set up your **product/service list**  

---

### Step 5: Add Your Leads
1. Put company names in the **Perusahaan** column  
2. Add contact names and emails (if available)  
3. Leave other fields empty → AI will fill them  
4. The workflow will **research each company**  

---

### Step 6: Test and Launch
1. Run the workflow **manually first**  
2. Check if **research results look good**  
3. Review the **generated emails**  
4. Activate the workflow for **automatic processing**  

---

## 🔄 How It Works
### Step 1: Company Research  
The workflow looks at each company in your sheet and searches the internet (via Tavily) to learn about their business, challenges, and opportunities.  

### Step 2: AI Analysis  
Using the research, GPT-4 analyzes the company and figures out:  
- What services might help them  
- What problems they may be facing  

### Step 3: Email Creation  
AI writes a **personalized email** mentioning specific things about their company and how you can help.  

### Step 4: Ready to Send  
The system creates a **clickable link** that lets you send the email with **one click** when you're ready.  

---

## 💡 Best Practices
- Research **5–10 companies at a time**, not hundreds  
- Always **review AI-generated emails** before sending  
- Keep your **service descriptions updated**  
- Check emails don’t sound too robotic  
- Follow up on responses **quickly**  

---

## 🎨 Customization Tips
- Modify the **AI prompts** to match your tone & style  
- Add more **research sources** for better data  
- Create **industry-specific templates**  
- Highlight your **unique value propositions**  
- Adjust the email tone (**formal vs casual**)  

---

## 🐞 Common Issues & Fixes
- ❌ **No research results** → Check your Tavily API key  
- ❌ **Generic emails** → Improve your email templates  
- ❌ **API errors** → Make sure you have OpenAI credits  
- ❌ **Sheet not updating** → Verify Google Sheets permissions  
- ❌ **Wrong company data** → Double-check spelling in company names  

---

## 🔒 Safety Tips
- ✋ Never send emails **without reviewing them first**  
- 📜 Always follow **anti-spam laws**  
- 🚫 Don’t research **competitors’ private info**  
- 🔑 Keep your **API keys secure**  
- 🔐 Respect companies’ **privacy policies**  
