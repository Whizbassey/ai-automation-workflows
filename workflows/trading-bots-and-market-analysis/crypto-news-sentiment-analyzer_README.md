# Crypto News Sentiment Analyzer 📈

Get instant news summaries and market feelings for any cryptocurrency! This smart tool reads news from 9 major crypto websites and tells you what people are saying about your favorite coins.

## What Does This Do? 🤔

Ever wonder what the crypto news is saying about Bitcoin, Ethereum, or any other coin? This workflow does the heavy lifting for you! Just send it a coin name, and it will:

- Find all recent news about that cryptocurrency
- Read articles from trusted crypto news sites
- Use AI to understand if the news is good or bad
- Give you a simple summary of what's happening

Think of it as your personal crypto news assistant that never sleeps!

## Cool Features ✨

- **Works with ANY crypto coin** - Bitcoin, Ethereum, Dogecoin, you name it!
- **Reads 9 different news sites** at once (CoinTelegraph, CoinDesk, Bitcoin Magazine, and more)
- **Smart AI analysis** using GPT-4o to understand market feelings
- **Quick responses** - get your summary in seconds
- **Easy to use** - just send a simple message with the coin name
- **Always up-to-date** - pulls the latest news every time

## What You Need First 📋

Before you can use this awesome tool, make sure you have:

- **N8N installed** (the automation platform)
- **OpenAI API key** (to power the AI analysis)
- **Internet connection** (to read the news sites)
- **Basic N8N knowledge** (how to import workflows)

## How to Set It Up 🛠️

### Step 1: Get Your OpenAI Key
1. Go to OpenAI's website and create an account
2. Get your API key from the dashboard
3. Keep it safe - you'll need it soon!

### Step 2: Import the Workflow
1. Open your N8N dashboard
2. Click "Import" and select this JSON file
3. The workflow will appear with all the nodes ready

### Step 3: Add Your API Key
1. Find the "OpenAI Chat Model" node
2. Click on it and add your API key
3. Do the same for the "Summarize News & Sentiment" node

### Step 4: Test It Out
1. Start the workflow
2. Send a POST request to the webhook with: `{"message": "bitcoin"}`
3. Watch the magic happen!

## How to Use It 🚀

It's super simple! Just send a message with any cryptocurrency name:

```json
{
  "message": "ethereum"
}
```

The workflow will automatically:
1. Figure out what coin you're asking about
2. Search through all the news sites
3. Find relevant articles
4. Analyze the sentiment
5. Send back a nice summary

## Example Response 📱

You'll get something like this:

```
Summary of News: Ethereum price has been stable this week...
Market Sentiment: Generally positive with some concerns about...
Links: [Links to the actual news articles]
```

## Want to Make It Better? 🔧

You can easily customize this workflow:

- **Add more news sources** - just add another RSS node
- **Change the AI model** - switch to GPT-3.5 to save money
- **Add Telegram alerts** - get notifications on your phone
- **Filter by date** - only look at news from the last 24 hours

## Need Help? 🆘

If something doesn't work:

1. Check your OpenAI API key is correct
2. Make sure all RSS feeds are working
3. Test with simple coin names like "bitcoin" first
4. Look at the error messages in N8N

## Credits 🙏

This workflow uses these amazing services:
- OpenAI for the smart analysis
- Multiple crypto news RSS feeds
- N8N for bringing it all together

Happy trading! Remember, this is just for information - always do your own research before making investment decisions! 💰

---

*Made with ❤️ for the crypto community*