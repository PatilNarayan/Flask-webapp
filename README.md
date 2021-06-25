# Flask-webapp
Deploy a web application on heroku using Git repository on local system.
		 
     
     - mkdir Flask-webapp 
		 - cd Flask-webapp
		 - python3 -m venv venv
		 - source venv/bin/activate
		 - python3 -m pip install Flask==1.1.2
		 - python3 -m pip freeze > requirements.txt
		 - vim app.py
		 		- [ 

		 				from flask import Flask

						app = Flask(__name__)

						@app.route("/")
						def index():
    						return "Hello World!"

    				]
    	 - flask run
    	 - git init
    	 - echo venv > .gitignore
    	 - echo __pycache__ >> .gitignore
    	 - git add .gitignore app.py requirements.txt
    	 - git commit -m "Initialize Git repository"
    	 - heroku login    #(If not login us this command)
    	 - echo "web: gunicorn app:app" > Procfile
    	 - python3 -m pip install gunicorn==20.0.4
    	 - python3 -m pip freeze > requirements.txt
    	 - git add Procfile requirements.txt
    	 - git commit -m "Add Heroku deployment files"
    	 - heroku create flask-webapp
    	 - git push heroku master
    	 - heroku open  # Web-app Will be open

    	 # app to github remote main
    	 - git remote add origin https://github.com/PatilNarayan/Flask-webaspp.git  #github repository HTTPS Link
    	 - git branch -M main 
    	 - git push -u origin main   # Enter UserName or Password
    	  
    	 # DONE !!! 
