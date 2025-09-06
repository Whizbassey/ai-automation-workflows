# Upwork Lead Generator & Email Finder

## Overview
This workflow automatically finds new Upwork job postings, figures out who posted them, then hunts down their email addresses using LinkedIn and other tools. Perfect for freelancers who want to reach clients directly instead of competing on Upwork.

---

## What It Does
- **Checks Upwork for new job postings** every few hours  
- **Uses AI** to find client names or company names in job descriptions  
- **Searches LinkedIn** to find their profiles  
- **Gets email addresses** using Hunter.io  
- **Saves everything to Google Sheets** for outreach  

---

## Features
- **Automatic Job Monitoring**: Runs on schedule to find fresh opportunities  
- **AI-Powered Name Extraction**: Smart detection of client names in job posts  
- **LinkedIn Integration**: Finds social profiles for better context  
- **Email Discovery**: Uses multiple tools to find contact information  
- **Lead Organization**: Saves all data in spreadsheets for follow-up  

---

## How the Process Works
1. **Job Collection**: Pulls latest jobs from Upwork using Apify  
2. **Name Detection**: AI reads job descriptions to find client names  
3. **Classification**: Determines if it's a person or company name  
4. **LinkedIn Search**: Uses Phantombuster to find profiles  
5. **Profile Scraping**: Gets detailed info from LinkedIn profiles  
6. **Email Finding**: Uses Hunter.io to discover email addresses  
7. **Data Storage**: Saves everything to Google Sheets  

---

## What You Need Before Starting
- **n8n automation platform**  
- **Apify account** (for Upwork scraping)  
- **Phantombuster account** (for LinkedIn search)  
- **Hunter.io account** (for email finding)  
- **OpenAI API key** (for AI processing)  
- **LinkedIn session cookie** (for scraping)  
- **Google Sheets** (for storing results)  

---

## API Requirements

### Apify Setup
- Create **Upwork job scraping task**  
- Get your **API token** and **task ID**  

### Phantombuster Setup
- Set up **LinkedIn People Search agent**  
- Set up **LinkedIn Profile Scraper agent**  
- Get your **API key** and **agent IDs**  

### Hunter.io Setup
- Sign up for **email finding service**  
- Get your **API key**  

### LinkedIn Cookie
- You need your **LinkedIn session cookie** for scraping  
- This allows the tools to access LinkedIn data  

---

## Installation Steps
1. Import the workflow JSON file into **n8n**  
2. Replace all placeholder API keys and IDs:  
   - `<TASK_ID>` – Your Apify task ID  
   - `<API_TOKEN>` – Your Apify API token  
   - `<AGENT_ID>` – Your Phantombuster agent IDs  
   - `<YOUR_API_KEY>` – Your various API keys  
   - `<LINKEDIN_SESSION_COOKIE>` – Your LinkedIn cookie  
3. Connect your **Google Sheets** for data storage  
4. Test with a **small batch** first  
5. Set up the **schedule trigger** for automatic runs  

---

## Workflow Logic
The system is smart about processing:  
- **Name Found**: Only processes jobs where it can identify a client name  
- **Person vs Company**: Treats individual clients and companies differently  
- **LinkedIn Search**: Uses different strategies for people vs companies  
- **Email Methods**: Company domain search vs personal email finding  

---

## Data Collected
For each lead, you get:  
- Original job title and description  
- Client/company name  
- LinkedIn profile information  
- Website/domain (for companies)  
- Email addresses found  
- Job posting details  

---

## Scheduling Options
You can set the workflow to run:  
- Every few hours for fresh leads  
- Daily for regular monitoring  
- Custom intervals based on your needs  

---

## Important Legal Notes
- Only scrapes **publicly available information**  
- Respects platform **terms of service**  
- Use responsibly for **legitimate business outreach**  
- Don’t spam or harass potential clients  
- Follow all relevant **privacy laws**  

---

## Success Tips
- Focus on jobs that **match your skills**  
- Personalize outreach based on **LinkedIn info**  
- Mention the specific **Upwork job** in your email  
- Keep initial contact **professional and brief**  
- Build relationships, don’t just pitch services  

---

## Customization Options
You can modify:  
- Job search **criteria and filters**  
- How often the workflow runs  
- Which **data fields** to collect  
- Email **templates** for outreach  
- LinkedIn **search parameters**  

---

## Troubleshooting
Common issues:  
- **API Rate Limits**: Add delays between requests  
- **Cookie Expiration**: Update LinkedIn session cookies regularly  
- **No Names Found**: AI might need better prompting  
- **Email Not Found**: Try different Hunter.io search methods  

