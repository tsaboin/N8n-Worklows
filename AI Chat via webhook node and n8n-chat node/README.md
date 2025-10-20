### How It Works

This N8n workflow integrates an AI assistant, Pallie, with office tools for tasks like email, calendar, and meetings. It starts with triggers: a webhook for incoming requests and a chat message receiver for direct interactions. When triggered, it routes data to an edit fields node for processing. Then it connects to tools: one for sending mail via MCP and another for calendar management. The assistant handles email, calendars, tasks, documents, research, travel, procurement, HR/IT, and general office ops with a polite, professional tone. It avoids guessing facts and offers next steps proactively. Emails must be in HTML with a specific signature from Lucidus Fortis which you should edit to your company.

### How to Use It

1. Set up the workflow in N8n by importing this JSON file. Ensure nodes link as shown: Webhook1 and When chat message received feed into Edit Fields.
2. Configure the webhook for external inputs, like API calls or forms. 
3. For chat integration, set up the "When chat message received" node to capture user queries.
4. Test the edit fields node to filter or format data before passing to tools.
5. Use the Send Mail Tool to send emails: point to your MCP endpoint for AWS SES, Zoho Mail or similar.
6. Apply the Calendar Tools for scheduling: link to your calendar MCP server.
7. Interact as Pallie: Send queries via chat or webhook to get help with office tasks. For example, ask "Schedule a meeting" to trigger the calendar tool.

### Optional

You can access this workflow as an OpenAI-compatible endpoint by giving a tag like "aimodel" and connect to it using this workflow here https://n8n.io/workflows/9438-create-universal-openai-compatible-api-endpoints-for-multiple-ai-workflows/
