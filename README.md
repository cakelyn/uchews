# CLOUD DATABASE SETUP #
1. setup an account at mlab.com
2. in your dashboard, click creat new under MongoDB Deployments
3. select amazon as your cloud provider and select sandbox as your plan type
4. select US as your AWS region
5. name your database, and submit your order
6. in your dashboard, selet your newly created database
7. click on users and add a user
8. inside your .env file add:
    DB_USER=[username]
    DB_PASS=[password]

# API key setup #
1. create a Google API key
2. enable Google Places API Web Service
3. enable Google Maps Geocoding API
4. enable Google Maps JavaScript API
5. inside Credentials, select the api key
6. select HTTP referrers (web sites) under Application Restrictions
7. add the following urls to Accept requests from these HTTP referrers (web sites) (Optional):
    *127.0.0.1:1337
    *frozen-beach-49440.herokuapp.com*
8. inside of your .env file add:
    GOOGLE_API_KEY=[api key]
9. inside of map.jsx insert your API key as a string on line 86

# OAuth 2.0 client ID#
This is necessary to enable Google sign-in
1. create a client ID from console.developers.google.com for OAuth 2.0 client IDs
  https://developers.google.com/identity/sign-in/web/devconsole-project is a helpful tutorial
2. set the GOOGLE_CLIENT_ID, GOOGLE_CLIENT_SECRET, and LOCAL_GOOGLE_REDIRECT variables in your .env file
  these three variables are all accessed in server/index.js when the GoogleStrategy is defined for passport
3. pay attention to step 5 in the tutorial above: you must authorize separate redirect urls for testing on your local machine and the deployed website


# HELPFUL RESOURCES #
AXIOS
https://github.com/axios/axios
EXPRESS
https://expressjs.com/
GOOGLE MAPS API REFERS
https://techjourney.net/google-maps-api-referrer-not-allowed-error/
MATERIAL-UI
http://www.material-ui.com/#/
MONGOOSE
http://mongoosejs.com/docs/index.html
PASSPORT
http://www.passportjs.org/docs
REACT
https://reactjs.org/docs/components-and-props.html
WEBPACK
https://webpack.js.org/