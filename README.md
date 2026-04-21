Text-to-SQL lets you ask questions in plain English and turns them into database commands, so you can work with your data without coding. In this read me, I’ll show you how to build a Text-to-SQL app that takes your questions, uses AI to translate them, runs the database query, and gives you the answer.
**Build a Text-to-SQL App**
Here’s the tech stack we’ll use:

Python: This will connect all the parts of our project.
Ollama: This tool lets you run powerful language models like Llama 3 or Mistral on your computer.
LangChain: This framework connects the AI to our database.
Streamlit: This Python library turns scripts into web apps you can share in minutes.
SQLite: A simple database that comes with Python, so you don’t need to install anything extra.

**Step 1: The Setup**
Pull the llama 3 model from Ollama:
Make a new folder for the project and run the below:
pip install langchain langchain-community langchain-ollama streamlit

**Step 2: Creating the Database**
We’ll write a simple Python script to make a sample SQLite database with student grades.
Create a file called create_db.py and run it once.
Run the python file and you’ll see a file called student_grades.db show up in your folder.

**Step 3: The Logic**
Now we’ll use LangChain to connect our local Llama 3 model to the database.
Create a file called app.py
Here, SQLDatabase.from_uri gives the database file to LangChain. Setting temperature=0 keeps the AI from being creative with SQL syntax, so it stays precise.

**Step 4: The User Interface**
 Finish app.py by adding the input box and the code to run your queries. Add this to your file:
 Next, open your terminal and start the Streamlit app:
 Try asking:
 “Show me all grades for Aman.”
“What is the average score in Math?”
“Who got a D?”
You’ll see the AI write the SQL, run it, and show you the result!

This tool helps in writing simple SQL queries for business managers. When you build tools like this, especially with bigger, secure databases like Postgres or Snowflake, you help non-technical teams get answers on their own, right away.
