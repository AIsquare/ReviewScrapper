# ReviewScrapper
![](review.png)
## Review scraper from scratch till deployment
### 1.	Prerequisites:
The things needed before we start building a python based web scraper are:
1.	Python installed.
2.  A Python IDE (Integrated Development Environment): like PyCharm, Spyder, or any other IDE of choice (Explained Later)
3.	Flask Installed. (A simple command: pip install flask)
4.	MongoDB installed (Explained Later).
5.	Basic understanding of Python and HTML.
6.	Basic understanding of Git (download Git CLI from https://gitforwindows.org/ )
![](arch.jpg)
6.	Heroku Basics:
1.	We’ll first go to heroku.com, and we’ll create a new account if we already don’t have one.
2.	We’ll download and install the Heroku CLI from the Heroku website: https://devcenter.heroku.com/articles/heroku-cli.
## 7.	Steps before cloud deployment:
We need to change our code a bit so that it works unhindered on the cloud, as well.
1. Add a file called ‘gitignore’ inside the ‘reviewScrapper’ folder. This folder contains the list of the files which we don’t want to include in the git repository. My gitignore file looks like:
.idea
As I am using PyCharm as an IDE, and it’s provided by the Intellij Idea community, it automatically adds the .idea folder containing some metadata. We need not include them in our cloud app.
2. 	Add a file called ‘Procfile’ inside the ‘reviewScrapper’ folder. This folder contains the command to run the flask application once deployed on the server:

web: gunicorn app:app
Here, the keyword ‘web’ specifies that the application is a web application. And the part ‘app:app’ instructs the program to look for a flask application called ‘app’ inside the ‘app.py’ file. Gunicorn is a Web Server Gateway Interface (WSGI) HTTP server for Python.

