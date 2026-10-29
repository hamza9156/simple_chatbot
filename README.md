# Simple n8n AI Chatbot

My first AI chatbot project built with **n8n**, **Google Gemini**, and **Simple Memory**.

The workflow receives a chat message, passes it to an AI Agent powered by Google Gemini, and connects Simple Memory to the agent to support conversational context.

## Workflow Overview

The workflow contains these nodes:

1. **When chat message received** — starts the workflow when a user sends a message through the n8n chat trigger.
2. **AI Agent** — handles the incoming message and generates a response.
3. **Google Gemini Chat Model** — provides the language model used by the AI Agent.
4. **Simple Memory** — provides conversational memory to the AI Agent.

### Workflow flow

```text
When chat message received
          |
          v
       AI Agent <----- Google Gemini Chat Model
          ^
          |
     Simple Memory
```

## Requirements

- An n8n instance (cloud or self-hosted)
- A Google Gemini API key and access to a compatible Gemini model
- Google Gemini credentials configured in n8n

## Import the Workflow into n8n

1. Download `simple-chatbot.json` from this repository.
2. Open your n8n workspace.
3. Create or open a workflow.
4. Use the workflow menu to **Import from File** and select `simple-chatbot.json`.
5. Open the **Google Gemini Chat Model** node and select or create your Google Gemini credentials.
6. Check the AI Agent and Simple Memory connections.
7. Save the workflow and test it using the chat interface.
8. Activate the workflow only after you have tested it and confirmed your configuration.

> The exported workflow does not include your API key. You must configure credentials in your own n8n account.

## Configure Google Gemini Credentials

1. In n8n, open **Credentials** and create the Google Gemini credential supported by your installed node version.
2. Add your Gemini API key in n8n's credential form.
3. Save the credential.
4. Select that credential in the **Google Gemini Chat Model** node.

**Never commit API keys, passwords, or credential exports to GitHub.**

## Repository Structure

```text
simple-n8n-chatbot/
├── README.md
└── simple-chatbot.json
```

## Notes

- This is a beginner project intended for learning and experimentation.
- Node names and available options may vary slightly depending on your n8n version.
- Simple Memory behavior depends on the memory node configuration and how the chat session is managed.
- Review the workflow and test it in your own n8n environment before using it for real users.

## Built With

- [n8n](https://n8n.io/)
- Google Gemini
- n8n AI Agent
- n8n Simple Memory

## Author

Created as my first n8n chatbot project.
