#HEROKU INTRO

Heroku lets us have our application running 24/7 on the web. First we need to setup a heroku account.
1) Once that's ready, we need to add the files that we want to include in our server to the github staging area.
2) now commit these files.
3) We need to make sure that in our package.json, we include a "start" under scripts and set it equal to "node app.js" so
that the Heroku server knows where to begin running the application.
4) Next, we login using "heroku login" in our terminal and create an app on heroku using "heroku create."
5) You will be given a url at the end after heroku manually installs npm and all the other packages that are listed under the dependencies of the package.json.
6) If there is an error, you will see an error occur during heroku create or when you visit the url itself.
7) You can check heroku logs to see if anything went wrong

URL for this app: https://lit-cove-48849.herokuapp.com/

logging in to heroku:

    heroku login
    --asks you for credentials (username/password)
    
create a heroku application:

    heroku create
    --adds remote for you. check it out with git remote -v
    
how to add all files to heroku:

    git push heroku master
    --pushes all the files that are tracked by git on your end
    
debugging heroku:

    heroku logs
    --heroku doesn't show you errors from url if something went wrong
    --heroku logs lets you see the errors that go on through the terminal
    
changing heroku environment variables:

    heroku config:set <KEY>=<secretkey>