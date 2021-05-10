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

 Using `pip freeze > requirements.txt` to create a txt file that tells heroku what packages to install for deployment purposes.

 Run `heroku login`
 if you get an "IP address mismatch error" on your browser, return to the terminal and close the running login operation with `ctrl c` and then run `heroku login -i` to sign into heroku from your terminal.

Logged in? Fantastic!, its time to create our app on heroku...simply run: `heroku create`

I know, the web address is funny..lol, well...heroku actually provides us the needed ability to change that url to something we love. to change te url, orun `heroku rename whitebokx` where "whitebokx" is the name of my url. if its already taken, you have to keep modifying your choice name until you find something suitable.


Now run `git push heroku main` to deploy your flask app to heroku. 

Congratulations!!



