# Website Email Scraper

## Overview
This workflow finds all public email addresses from any website automatically. Just enter a website URL and it will search through pages like **About**, **Contact**, **Team**, and **Company** to collect email addresses for you.

---

## What It Does
- **Takes a website URL** from a simple form  
- **Maps the website** to find relevant pages (about, contact, team pages)  
- **Scrapes pages** for email addresses  
- **Finds hidden emails** (like `name(at)company(dot)com` formats)  
- **Returns a clean list** of all email addresses found  

---

## Features
- **Smart Page Finding**: Automatically looks for contact and team pages  
- **Email Detection**: Finds emails even when they're disguised to avoid spam  
- **Clean Results**: Removes duplicates and invalid addresses  
- **Form Interface**: Easy-to-use form for entering website URLs  
- **Batch Processing**: Can handle multiple pages at once  

---

## What You Need Before Starting
- **n8n automation platform**  
- **Firecrawl API account** (for website scraping)  
- **A website URL** to test with  

---

## How It Works
1. You enter a website URL in the form  
2. The workflow maps the website to find contact/about pages  
3. Firecrawl scrapes all relevant pages  
4. AI extracts and cleans up email addresses  
5. You get a list of all emails found  

---

## Email Formats It Finds
The scraper can detect emails written as:  
- **Normal format**: `user@company.com`  
- **Hidden format**: `user(at)company(dot)com`  
- **Spaced format**: `user at company dot com`  
- **HTML encoded**: `user&#64;company&#46;com`  

---

## Installation Steps
1. Import the workflow JSON file into **n8n**  
2. Get your **Firecrawl API key** from [firecrawl.dev](https://firecrawl.dev)  
3. Add your API key to the **HTTP Request nodes**  
4. Test with a website that has visible contact information  
5. Use the **form interface** to scrape websites  

---

## API Setup
You need to:  
- Sign up at [Firecrawl.dev](https://firecrawl.dev)  
- Get your **API key**  
- Replace the **placeholder API key** in all HTTP nodes  
- Set up authentication headers  

---

## Rate Limiting
The workflow includes:  
- **Automatic retry logic** (up to 12 attempts)  
- **Wait periods** between requests  
- **Error handling** for timeouts  

---

## Results
The workflow returns:  
- Array of **unique email addresses**  
- **Cleaned and validated** emails only  
- No duplicates or fake examples  

---

## Use Cases
- Finding contact information for outreach  
- Building email lists from competitor websites  
- Research for business development  
- Collecting emails from company websites  

---

## Important Notes
- Only scrapes **publicly available information**  
- Respects **robots.txt** and rate limits  
- Does **not** access private or protected content  
- Use responsibly and follow **website terms of service**  


