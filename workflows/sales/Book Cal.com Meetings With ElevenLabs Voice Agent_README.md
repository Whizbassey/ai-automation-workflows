# Book Cal.com Meetings from ElevenLabs Voice Agent Conversations

## Overview
This workflow lets your AI voice agent automatically book meetings in Cal.com when talking to potential customers. When someone wants to schedule a call during a voice conversation, the AI can instantly create the booking without human help. It's like having a smart receptionist that never sleeps!

## What It Does
- 🎙️ Receives booking requests from ElevenLabs voice agents
- ✅ Checks if all required information is provided
- 📅 Creates meetings directly in Cal.com
- 🔒 Uses secure authentication for safety
- ⚡ Responds instantly to voice agents
- 📝 Handles booking confirmation automatically

## What You Need Before Starting
- N8N installed and running
- Cal.com account with API access
- ElevenLabs voice agent setup
- Cal.com API key
- Webhook authentication token
- Basic understanding of voice AI systems

## Setup Instructions

### Step 1: Get Your Cal.com API Key
1. Log into your Cal.com account
2. Go to Settings > Developer
3. Create a new API key
4. Copy the key (starts with "cal_live_")
5. Save it securely - you'll need this later

### Step 2: Set Up Your Cal.com Event Types
1. Create event types for different meeting types
2. Note down the Event Type IDs (you'll see these in the URL)
3. Set your availability and meeting duration
4. Configure any required booking fields

### Step 3: Import and Configure Workflow
1. Copy the JSON workflow content
2. Import it into N8N
3. Replace "cal_live_replace_me_with_api_key" with your real API key
4. Change "validate-booking-1234-abcd" to your own secure path
5. Set up header authentication with a secret token

### Step 4: Configure Your ElevenLabs Voice Agent
1. Set up your voice agent to collect these details:
   - Customer name
   - Email address
   - Phone number
   - Company name
   - Meeting notes/reason
   - Preferred meeting time
   - Timezone
2. Program it to send this data to your N8N webhook

### Step 5: Test the Integration
1. Test the webhook manually with sample data
2. Try a conversation with your voice agent
3. Check if meetings appear in your Cal.com calendar
4. Verify confirmation emails are sent
5. Test error handling with incomplete data

### Step 6: Go Live
1. Update your voice agent with the live webhook URL
2. Monitor the first few bookings carefully
3. Set up alerts for any failures
4. Train your team on the new automated process

## How It Works

### The Booking Process
1. **Voice Conversation**: Customer talks to your ElevenLabs AI agent
2. **Data Collection**: AI gathers all required booking information
3. **Webhook Call**: Voice agent sends booking request to N8N
4. **Validation**: Workflow checks if all required fields are present
5. **Booking Creation**: If valid, creates meeting in Cal.com
6. **Response**: Sends success or error message back to voice agent
7. **Customer Confirmation**: Cal.com sends confirmation email to customer

### Required Information for Booking
The voice agent must collect:
- **attendee_name**: Customer's full name
- **attendee_email**: Valid email address
- **attendee_phone**: Phone number
- **attendee_company**: Company name
- **attendee_timezone**: Customer's timezone
- **start**: Meeting date and time
- **eventTypeId**: Which type of meeting to book
- **notes**: Reason for meeting or special requests

## Customization Options
- Add more required fields for booking
- Create different event types for different services
- Set up automatic follow-up emails
- Connect to CRM systems
- Add SMS notifications
- Include meeting preparation materials

## Error Handling
The workflow handles these situations:
- **Missing Information**: Tells voice agent to get more details
- **Invalid Data**: Returns specific error messages
- **Booking Conflicts**: Cal.com handles scheduling conflicts
- **API Errors**: Returns clear error responses

## Security Features
- **Webhook Authentication**: Only authenticated requests are processed
- **Data Validation**: All input is checked before processing
- **API Key Protection**: Secure handling of sensitive credentials
- **Response Filtering**: Only necessary information is returned

## Best Practices
- Keep your API key secure and never share it
- Use HTTPS for all webhook communications
- Test regularly to ensure everything works
- Monitor booking success rates
- Train your voice agent to get complete information
- Set up backup procedures for system failures

## Troubleshooting
- **No bookings created**: Check your Cal.com API key and permissions
- **Voice agent not connecting**: Verify webhook URL and authentication
- **Incomplete bookings**: Make sure voice agent collects all required fields
- **Calendar conflicts**: Check your Cal.com availability settings
- **Authentication errors**: Verify your header authentication token

## Voice Agent Training Tips
Train your AI to:
- Ask for all required information naturally
- Confirm details before booking
- Handle time zone conversions properly
- Explain next steps to customers
- Gracefully handle booking failures
- Offer alternative times if needed

## Monitoring and Analytics
- Track booking success rates
- Monitor which voice conversations lead to bookings
- Identify common failure points
- Measure customer satisfaction
- Review booking completion rates
- Analyze popular meeting times