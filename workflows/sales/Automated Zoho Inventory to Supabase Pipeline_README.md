# Automated Zoho Inventory to Supabase Product Data Pipeline

## Overview
This workflow automatically copies all your product data from Zoho Inventory into a Supabase database on a schedule. It keeps your product information updated across different systems without manual work. Great for businesses that need their inventory data in multiple places!

## What It Does
- 🔄 Runs automatically on a schedule you set
- 🔑 Gets fresh access tokens from Zoho API
- 📦 Pulls all product data from Zoho Inventory
- 🗃️ Stores everything in your Supabase database
- 📊 Keeps product information synchronized
- ⚡ Handles large inventories efficiently

## What You Need Before Starting
- N8N installed and running
- Zoho Inventory account with products
- Supabase account and database
- Zoho API credentials (Client ID, Client Secret, Refresh Token)
- Supabase connection details
- Basic understanding of API keys

## Setup Instructions

### Step 1: Create Zoho API Application
1. Go to Zoho API Console (console.zoho.com)
2. Click "Add Client" and choose "Self Client"
3. Set the scope to: `ZohoInventory.items.READ`
4. Generate your Client ID and Client Secret
5. Get your Refresh Token (this stays active longer)
6. Find your Organization ID in Zoho Inventory settings

### Step 2: Set Up Supabase Database
1. Create a new project in Supabase
2. Create a table called "Fairy Frills" (or change the name in workflow)
3. Add these columns to match Zoho data:
   - Product ID, Product Name, Brand
   - Variant ID, Variant Name, SKU
   - Stock On Hand, Status
   - All the attribute fields
   - Created Time, etc.

### Step 3: Import and Configure Workflow
1. Copy the JSON workflow content
2. Import it into N8N
3. Update these values with your real information:
   - `your refresh token here`
   - `your client id here`
   - `your client secret here`
   - `your organization id here`
4. Connect your Supabase credentials

### Step 4: Set Your Schedule
1. Open the "Scheduled Trigger" node
2. Choose how often you want updates:
   - Every hour for fast-moving inventory
   - Daily for most businesses
   - Weekly for stable products
3. Pick a time when your system isn't busy

### Step 5: Test the Connection
1. Run the workflow manually first
2. Check if you get an access token from Zoho
3. Verify products are fetched from Zoho
4. Confirm data appears in your Supabase table
5. Make sure field mapping is correct

### Step 6: Activate and Monitor
1. Activate the workflow in N8N
2. Check the first few scheduled runs
3. Monitor for any errors
4. Verify data quality in Supabase

## How It Works

### The Process Flow
1. **Schedule Trigger**: Starts the workflow at your chosen time
2. **Get Access Token**: Uses your refresh token to get a new access token
3. **Fetch Products**: Gets all inventory items from Zoho
4. **Split Data**: Breaks down the product list for easier processing
5. **Save to Supabase**: Stores each product in your database

### Important Details
- Access tokens expire, so we get fresh ones each time
- The workflow handles pagination automatically
- All product variants are included
- Data is completely replaced each run (not merged)

## Customization Options
- Change the Supabase table name and structure
- Add data transformation before saving
- Filter products by category or status
- Include additional Zoho fields
- Set up error notifications
- Add data validation checks

## Field Mapping Reference
The workflow maps these Zoho fields to Supabase:
- `group_id` → Product ID
- `group_name` → Product Name  
- `item_id` → Variant ID
- `item_name` → Variant Name
- `sku` → SKU
- `stock_on_hand` → Stock On Hand
- And many more attributes and details

## Troubleshooting Guide
- **No access token**: Check your refresh token and client credentials
- **No products returned**: Verify your organization ID
- **Supabase connection fails**: Check your database credentials
- **Field mapping errors**: Make sure Supabase table columns match
- **Timeout issues**: Try running during off-peak hours

## Best Practices
- Test with a small product set first
- Keep your API credentials secure
- Monitor your API usage limits
- Set up backup procedures
- Document any customizations
- Check data accuracy regularly

## Security Notes
- Never share your refresh token or client secret
- Use environment variables for sensitive data
- Regularly rotate your API credentials
- Monitor API access logs
- Limit database access permissions
- Use secure connections only