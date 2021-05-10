/Whitebox
A students digital notepad.

//Set Up and Installations

Ensure that you have the following packages installed:
- Python 3.6 and above
- git for version control
- an account on github.com

// Deployment to Heroku
follow the installation for heroku and heroku CLI here to install the latest version 
`https://devcenter.heroku.com/articles/heroku-cli`

 install gunicorn with `pip install gunicorn`
 let heroku know you are using the gunicorn package by creating a procfile.
 `touch Procfile`
 NB: the Procfile is a no extension named file(i.e, it has no extensions of any sort, e.g .txt, .md...etc), also ensure that this file is created within the root directory of your project as it doesnt function anywhere else.

 within the Procfile, type in the following;
 `web: gunicorn main:app`
 i used `main` in the above command because my application root entry is called main.py, if yours is app.py then it should be called `app` or something else that you might ave chosen to call your application

 Using `pip freeze > requirements.txt` to create a txt file that tells heroku what packages to install for deployment purposes
 


