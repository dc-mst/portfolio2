---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Python golf: leave a message"
url: "/leave-a-message"
subtitle: "simple web app to store messages in a database"
summary: "Create a Python app that in less than 30 lines of code"
authors: [ d-cmst ]
tags: [ Python, Code golf, Web, SQL ]
categories: [ Python, Code golf ]
keywords: [Python, Code golf, SQL ]
date: 2023-05-16
publishDate: 2023-05-16
lastmod: 2023-05-16
featured: false
draft: false


# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

I stumbled upon this (python) code-golf  question:

> Can I code a simple Flask app that gets messages from a web page and stores them in a database?

With Python/Flask it's actually easier done than said!

## The code

```python
from flask import Flask, render_template, request
import sqlite3

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///notes.db'

@app.route('/', methods=['GET', 'POST'])
def index():
    title = "Send a message"
    db = sqlite3.connect('notes.db')
    cursor = db.cursor()

    if request.method == 'POST':
        message = request.form['content']
        cursor.execute('INSERT INTO notes (message) VALUES (?)', (message,))
        db.commit()
        db.close()
        return render_template("message-sent.html.j2", title=title)

    cursor.execute('SELECT COUNT(*) FROM notes')
    count = cursor.fetchone()[0]
    db.close()

    return render_template("index.html.j2", count=count, title=title)

if __name__ == "__main__":
    app.run(debug=True)

```

Just 775 characters in twenty-seven lines of code. Now let's try to explain what it does:

## The explanation

_This code sets up a Flask web application with an SQLite database called notes.db. The application has only one route, the index route '/'. When a GET request is made to the '/' page, it connects to the notes.db database and fetches the total number of messages in the database. It then displays the fetched message count using a Jinja2 template called index.html.j2._

_When a POST request is made to the '/' route, it connects to the notes.db database, inserts the submitted message into the 'notes' table, and redirects the user to a success message page using the message-sent.html.j2 Jinja2 template._

604 characters! This Python code is actually almost as concise as the plain English description of what it does.

