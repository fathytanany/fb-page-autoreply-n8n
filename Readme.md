# Facebook Page Auto Reply Bot (n8n)

This project is an automated Facebook Messenger bot built using [n8n](https://n8n.io/).  
It listens for new messages sent to a Facebook Page and sends back automated replies.

## ✨ Features
- Auto-replies to all incoming messages on a Facebook Page
- Personalizes responses using the sender’s first name
- Runs locally using ngrok or Cloudflare Tunnel
- Works with n8n’s no-code/low-code environment

## 📋 Requirements
- Facebook Page & Admin access
- Facebook Developer account
- Page Access Token
- n8n installed locally
- ngrok (or Cloudflare Tunnel) for public webhook URL

## 🚀 Setup Instructions
### 1. Install n8n
```bash
npm install -g n8n
n8n
```
 
or run with docker 
```
docker run -it --rm \
  --name n8n \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
```

### 2. Start ngrok (or Cloudflare Tunnel)
 ```
ngrok http 5678
```
Copy the HTTPS URL ngrok gives you (e.g., https://myname.ngrok.io).

### 3. Set up Facebook App
Create an app at Meta for Developers.

Add Messenger product.

Link your Facebook Page.

Generate a Page Access Token.

Subscribe your webhook to messages and messaging_postbacks.

### 4. Import the Workflow
Download workflow.json from this repo.

In n8n, click Import from File and select workflow.json.

Update the HTTP Request node to use your Page Access Token.

### 5. Activate the Workflow
Click Activate in n8n.

Send a message to your Page from another Facebook account to test.

🔒 Privacy
We take user privacy seriously. See privacy-policy.md for details.