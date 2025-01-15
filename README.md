**Graph-Based Editor for LLM Workflows**

![Hero](https://github.com/user-attachments/assets/d2f9f74d-98f6-492b-895c-7bf8a83b6c17)


**✨ Core Benefits**

**Modular Building Blocks**

![Blocks](https://github.com/user-attachments/assets/c8707b3c-0e5d-4a45-a50a-a57fddc7909b) 


**Evaluate Final Performance**

![evals](https://github.com/user-attachments/assets/32dd2a48-1da0-44ae-9080-72ab1b3ad7c9)


**Coming soon: Self-improvement**

![Optimization](https://github.com/user-attachments/assets/aad1ea5f-e141-4726-bd46-d0c3b0b4c772)


**🕸️ Why Slack?**
Easy-to-hack, eg., one can add new workflow nodes by simply creating a single Python file.
JSON configs of workflow graphs, enabling easy sharing and version control.
Lightweight via minimal dependencies, avoiding bloated LLM frameworks.

**⚡ Quick start**
You can launch Slack using pre-built docker images in the following steps:

**Clone the repository:**

git clone https://github.com/Slack/Slack.git
cd Slack
Create a .env file:

Create a .env file at the root of the project. You may use .env.example as a starting point.

cp .env.example .env
Please go through the .env file and change configs wherver necessary If you plan to use third party model providers, please add their API keys in the .env file in this step.

Start the docker services:

docker compose -f ./docker-compose.prod.yml up --build -d
This will start a local instance of Slack that will store spurs and other state information in a postgres database. A local postgres service is used by default. Override POSTGRES_* variables in the .env file to use an external postgres database.

Access the portal:

Go to http://localhost:6080/ in your browser.

Set up is completed. Click on "New Spur" to create a workflow, or start with one of the stock templates.

[Optional] Manage your LLM provider keys from the app:

Once Slack app is running you can manage your LLM provider keys through the portal:

Select API keys tab
