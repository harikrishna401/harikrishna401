- 👋 Hi, I’m @harikrishna401
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
harikrishna401/harikrishna401 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import nltk
import numpy as np
import regex as re

# Example: Simple FAQ chatbot
faqs = {
    'What is Python?': 'Python is a high-level programming language...',
    'How do I install Python?': 'You can install Python by downloading...',
    # Add more FAQs and answers
}

def respond(user_input):
    for question, answer in faqs.items():
        if re.search(question, user_input, re.IGNORECASE):
            return answer
    return "Sorry, I don't understand your question."

while True:
    user_input = input("You: ")
    if user_input.lower() == 'exit':
        break
    response = respond(user_input)
    print("Bot:", response)

import sqlite3

# Example: Simple SQLite CRUD application
conn = sqlite3.connect('example.db')
c = conn.cursor()

# Create table
c.execute('''CREATE TABLE IF NOT EXISTS users
             (id INTEGER PRIMARY KEY AUTOINCREMENT, name TEXT, age INTEGER)''')

# Insert data
c.execute("INSERT INTO users (name, age) VALUES (?, ?)", ('Alice', 25))
c.execute("INSERT INTO users (name, age) VALUES (?, ?)", ('Bob', 30))
conn.commit()

# Fetch and display data
c.execute("SELECT * FROM users")
rows = c.fetchall()
for row in rows:
    print(row)

conn.close()


import sqlite3

# Example: Simple SQLite CRUD application
conn = sqlite3.connect('example.db')
c = conn.cursor()

# Create table
c.execute('''CREATE TABLE IF NOT EXISTS users
             (id INTEGER PRIMARY KEY AUTOINCREMENT, name TEXT, age INTEGER)''')

# Insert data
c.execute("INSERT INTO users (name, age) VALUES (?, ?)", ('Alice', 25))
c.execute("INSERT INTO users (name, age) VALUES (?, ?)", ('Bob', 30))
conn.commit()

# Fetch and display data
c.execute("SELECT * FROM users")
rows = c.fetchall()
for row in rows:
    print(row)

conn.close()
