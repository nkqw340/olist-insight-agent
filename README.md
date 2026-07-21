# olist-insight-agent

**What this is**

This project involves the use of Anthropic to create a conversational AI agent that answers business questions about the Olist Brazilian e-commerce dataset by autonomously writing and executing SQL queries.

**How it works**

Two main functions are needed
1. sql_run_query connects to the dataset and tells the system to run queries produced by Claude
2. run_agent tells Claude how to run. It comprises of
   a. A list containing the history of the conversation which Claude will refer to for every call
   b. System prompt telling Claude the background and its role
   c. Tools Claude has access to and requirements to use the tool
   d. Loop that runs Claude until Claude stops to return the answer or run the tool
A simple user interface is included with functionalities to return the answer or the history.
   
**How to set up**
1. Clone the repo
2. pip install anthropic pandas
3. Download Olist dataset from Kaggle and place in data/ folder
4. Set your API key as an environment variable: export ANTHROPIC_API_KEY=your_key
5. Run: python agent.py (or in setup cell to load data first)

**Example questions**
1. What is the highest-rated category?
2. What is the repeat purchase rate?
3. What is the average delivery time for 1-star vs 5-star reviews?
