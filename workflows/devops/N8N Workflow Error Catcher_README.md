# Workflow Error Notification System

## Overview
This workflow acts like a safety net for all your other N8N workflows. When any of your workflows break or fail, this one jumps in and sends you a Telegram message right away. It's like having a personal assistant that tells you when something goes wrong!

## What It Does
- 🚨 Catches errors from any workflow
- 📱 Sends instant Telegram notifications
- 📝 Shows which workflow failed
- 🔗 Includes direct link to the problem
- ⚡ Works automatically with no setup needed for each workflow

## What You Need Before Starting
- N8N installed and running
- Telegram account
- Telegram bot token
- Your Telegram chat ID
- Other N8N workflows to monitor

## Setup Instructions

### Step 1: Create a Telegram Bot
1. Open Telegram and search for @BotFather
2. Start a chat and type `/newbot`
3. Follow the instructions to create your bot
4. Save the bot token you receive

### Step 2: Get Your Chat ID
1. Start a chat with your new bot
2. Send any message to it
3. Go to: `https://api.telegram.org/bot<YOUR_BOT_TOKEN>/getUpdates`
4. Look for your chat ID in the response

### Step 3: Import and Setup the Workflow
1. Import the JSON file into N8N
2. Open the Telegram node
3. Add your Telegram credentials
4. Replace the chat ID with your own
5. Save the workflow

### Step 4: Connect to Other Workflows
1. Go to any workflow you want to monitor
2. Click on workflow settings
3. Find "Error Workflow" option
4. Select this error notification workflow
5. Save your changes

### Step 5: Test and Activate
1. Test by creating a small error in another workflow
2. Check if you get the Telegram message
3. Activate this error workflow
4. Apply it to all important workflows

## How It Works
When any connected workflow fails, this workflow automatically starts. It creates a nice message with the workflow name and a link to see what went wrong. Then it sends this message to your Telegram chat instantly.

## Customization Ideas
- Change the message format to include more details
- Add email notifications too
- Send to multiple people or groups
- Include error details in the message

## Tips
- Keep this workflow always active
- Test it regularly to make sure it works
- Apply it to all important workflows
- Check your Telegram notifications are on