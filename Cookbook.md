# 🧑‍🍳 AI Data Analyst Chatbot Cookbook (E-Commerce Example)

## 🍲 Ingredients

- An n8n account (self-hosted or cloud)
- A Nebius AI Studio account
- Google Sheets & Docs API credentials (OAuth)
- A copy of your example Google Sheet (e-commerce transactions or similar)

## 🛠️ Setup & Integration

### 1. Configure n8n Environment

- Sign in to your n8n account.
- Create a new workflow or import `Nike AI Data Analyst Chatbot FINAL.json` (example workflow for e-commerce analytics).

### 2. Setup Nebius LLM Node

- Use `deepseek-ai/DeepSeek-V3-0324-fast` from Nebius AI Studio.
- Add your Nebius API Key in credentials.

### 3. Google Sheets Integration

- Add Google Sheets OAuth credentials in n8n.
- Use your own Google Sheets link in these nodes:
  - Get transactions by status
  - Get transactions by product name
  - Get all transactions

### 4. Google Docs Integration

- Create a Google Doc for strategic updates.
- Add Google Docs OAuth credentials.
- Paste your document URL into the "Document Strategy" node.

### 5. Workflow Overview Diagram

- See `assets/workflow-diagram.png` for a visual overview.

## 📈 Workflow Deep-Dive

### 🧠 AI Agent Node

- Nebius DeepSeek powers intelligent reasoning and data analysis.
- Responds with structured JSON:
  ```json
  {
    "reply": "Text response to user",
    "doc_update": "Content to update Google Doc"
  }
  ```

### 📗 Structured Output Parser

- Ensures Nebius model's output is correctly parsed as JSON.

### 🔎 Google Sheets Tools

- Dynamically retrieve data based on criteria:
  - Product Name
  - Transaction Status

### 📚 Buffer Memory

- Short-term memory (last 5 messages) ensures coherent conversations.

### 🖥️ Decision Nodes

- Conditionally process responses and document updates.

### 📌 Document & Chat Updates

- Updates strategic documents automatically.
- Provides clean, readable chat responses.

## 💡 Advanced Use Case Ideas

- **Sales Outreach Automation:** Check 100 target companies simultaneously, auto-merge insights.
- **Employee Knowledge Assistant:** Instant chatbot access to internal docs.
- **Real-Time Competitive Intelligence:** Continuously update competitive landscape docs.

## 🚀 Run Your Workflow

- Activate workflow and trigger via n8n chat interface or webhook.
- Start asking questions like:
  - "How many refunds in January and what was the amount refunded?"
  - "What's our most popular product?"

## 🛠️ Troubleshooting

- Ensure all credentials are correct and active.
- Check n8n logs for node errors.
- Validate Google API quotas and permissions.

## 📌 Additional Resources

- [Nebius AI Studio](https://studio.nebius.com/)
- [n8n Documentation](https://docs.n8n.io/)
- [Google OAuth n8n Setup Guide](https://docs.n8n.io/integrations/builtin/credentials/Google/)

---

Contributions welcome! 