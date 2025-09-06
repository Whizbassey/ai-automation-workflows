# Shopify Bulk Product Creator

## Overview
This workflow helps you quickly add lots of products to your Shopify store using data from a Google Sheet. It's perfect for setting up test stores, importing product catalogs, or trying out new store designs with real-looking data.

---

## What It Does
- **Reads product information** from Google Sheets  
- **Creates new products** in Shopify (skips products that already exist)  
- **Sets up inventory tracking** automatically  
- **Updates stock levels** for each product  

---

## Features
- **Smart Duplicate Check** – Won’t create the same product twice  
- **Inventory Management** – Automatically enables tracking and sets stock levels  
- **Batch Processing** – Handles multiple products in one go  
- **Error Prevention** – Skips existing products instead of creating duplicates  

---

## What You Need Before Starting
- A **Shopify store** with admin access  
- A **Google account** with Sheets  
- **N8N automation platform**  
- **Shopify API credentials**  

---

## Google Sheet Setup
Your sheet needs these column headers:  

| Column Name       | Description                                      |
|-------------------|--------------------------------------------------|
| `title`           | Product name                                     |
| `description`     | Product details                                  |
| `company`         | Brand or vendor name                             |
| `category`        | Product type                                     |
| `status`          | ACTIVE, DRAFT, or ARCHIVE                        |
| `slug`            | URL-friendly name (no spaces)                    |
| `price`           | How much it costs                                |
| `compare_at_price`| Original price for sales                         |
| `sku`             | Unique product code                              |
| `stock_on_hand`   | How many you have in stock                       |

---

## Installation Steps
1. Import the **workflow JSON file** into N8N  
2. Update all **GraphQL nodes** with your Shopify store URL  
3. Connect your **Google Sheets account**  
4. Add your **Shopify API credentials**  
5. Test with a **small batch** of products first  

---

## Important Notes
- Uses **Shopify’s 2025-04 GraphQL Admin API**  
- Products are matched by their **slug/handle** to prevent duplicates  
- All new products get **placeholder images** (you can change this later)  
- **Inventory tracking** is enabled automatically  

 
