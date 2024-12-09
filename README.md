Slack Bot with Wolfram Alpha and Wit.ai Integration
Overview
This bot integrates with Slack to answer user queries using Wolfram Alpha and Wit.ai. It leverages the power of natural language processing (NLP) and computational knowledge to provide detailed and accurate answers to user-submitted questions.

Features
Query Handling: Accepts user queries in a predefined format via Slack commands.
Natural Language Processing: Uses Wit.ai to parse and extract meaning from user input.
Computational Knowledge: Utilizes Wolfram Alpha to retrieve and return factual answers.
Real-Time Command Tracking: Logs and prints command events for analytics.
How It Works
Slack Command: Users type a command in Slack in the format:

graphql
Copy code
query for bot - <message>
Example: query for bot - Who is the president of India?

Wit.ai Processing: The bot sends the user's query to Wit.ai for natural language processing and extracts relevant data (e.g., search intent).

Wolfram Alpha Query: The bot uses the extracted information to query Wolfram Alpha for a precise and spoken response.

Reply in Slack: The bot responds directly in Slack with the answer retrieved from Wolfram Alpha.

Prerequisites
Slack Tokens:
Slack_Bot_Token: For bot authentication.
Slack_App_Token: For app-level access.
Wit.ai Token: To integrate NLP capabilities.
Wolfram Alpha App ID: For accessing Wolfram Alpha's API.
.env File: Ensure these tokens are stored in a .env file as environment variables.
Environment Variables
Add the following keys to your .env file:

makefile
Copy code
Slack_Bot_Token=your-slack-bot-token
Slack_App_Token=your-slack-app-token
WIT_AI_TOKEN=your-witai-token
WOLFRAM_APP_ID=your-wolfram-alpha-app-id
Usage
Start the bot using:
bash
Copy code
go run main.go
In Slack, type a command:
graphql
Copy code
query for bot - <your question>
The bot will respond with an answer fetched from Wolfram Alpha.
Example
Command:
query for bot - What is the speed of light?

Response:
The speed of light in a vacuum is approximately 299,792 kilometers per second.

Error Handling
If an error occurs while fetching data, the bot logs the issue and informs the user that something went wrong.
Dependencies
Slacker: For interacting with Slack.
Wit.ai: For natural language processing.
Wolfram Alpha API: For computational knowledge retrieval.
GJSON: For parsing JSON responses.
Godotenv: For managing environment variables.
Future Enhancements
Add support for more complex queries.
Include a fallback response for unsupported queries.
Improve error handling and user feedback.
