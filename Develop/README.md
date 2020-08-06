#reverse-engineering

--USER STORY--
As a user that has experienced password security threat. This app allows users to login safely with password encryption.

--TECH USED --
-BCRYPTJS -EXPRESS -EXPRESS-SESSION -MYSQL2 -PASSPORT -PASSPORT-LOCAL -SEQUELIZE

--PASSWORD AUTHENTICATION--
This app allows users to login safely with password encryption.. Data is stored through the mysql database.



--FILES EXPLAINED--
CONFIG/MIDDLEWARE
isAuthenticated.js is code written for restricting routes. If user is logged in then it takes them to the next (restricted) rout. If the user is not logged in then the code is taking them back to the landing page.

config.json is a file that define global values and dependacies. Allos access to the database.

passport.js is code that is having the user use their email as their username. It checks to see if email is in database, if it is not then it returns message "Incorrect email". It checks for a correct password, if password entered is wrong then it returns message "Incorrect password." Otherwise it returns the user.

MODELS
index.js this is our connection to the databse using Sequelize

user.js this is code creating tables with the database

ROUTES
api-routes.js Routes communcating with the database to get, post, put or delete information in the database

html-routes.js These are routes that will direct the user to certain html pages depending on user entries

package.json a file that is requiring any dependancies for application

server.js is where we are requiring express, require our html and api routes set up the PORT and syncing the database