# Squarespace Order Sync

## Overview
This workflow automatically pulls all your Squarespace orders and saves them to Google Sheets. It's great for keeping track of sales, analyzing customer data, or creating reports without manually copying information.

---

## What It Does
- **Connects to your Squarespace store**  
- **Downloads all order information**  
- **Saves everything to Google Sheets** in an organized way  
- **Runs on a schedule** to stay up-to-date  

---

## Features
- **Complete Order Data**: Gets customer info, shipping details, and order totals  
- **Smart Pagination**: Automatically handles stores with lots of orders  
- **Flexible Filtering**: Can filter by dates, order status, or other criteria  
- **Scheduled Updates**: Set it to run daily, weekly, or however often you need  
- **No Manual Work**: Runs automatically once set up  

---

## What You Need Before Starting
- A **Squarespace store** with orders  
- **Squarespace API access**  
- **Google account with Sheets**  
- **n8n automation platform**  

---

## Installation Steps
1. **Import** the workflow JSON file into n8n  
2. Open the **Globals node** to configure your settings:  
   - `api-version`: Set to `"1.0"` (current version)  
   - `modifiedAfter`: Date to start from (leave empty for all orders)  
   - `modifiedBefore`: End date (leave empty for all orders)  
   - `fulfillmentStatus`: `PENDING`, `FULFILLED`, `CANCELED`, or empty for all  
   - `maxPage`: Set to `-1` to get all orders, or limit the number  
3. Connect your **Squarespace API credentials**  
4. Link your **Google Sheets account**  
5. Test with a **small date range first**  

---

## Order Information Saved
The workflow saves these details for each order:
- Customer name, email, and phone  
- Billing and shipping addresses  
- Order totals and currency  
- Payment and shipping methods  
- Order status and fulfillment info  
- Individual product details  

---

## Scheduling Options
You can run this workflow:  
- **Manually**: Click *Execute* when you need fresh data  
- **Automatically**: Use the schedule trigger for regular updates  
- **On Demand**: Trigger from other workflows  

---


