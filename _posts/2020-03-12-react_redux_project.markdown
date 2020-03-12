---
layout: post
title:      "React / Redux Project"
date:       2020-03-12 13:52:32 +0000
permalink:  react_redux_project
---

With my React project, I was tasked with creating functional and class components that make good use of props and that work with the Redux store to save the information so that the app has everything in its store and does not require constant communication with the database.

My project, called Trip Planner, is a simple app that allows the user to create trips and save associated sites that they want to visit along their travels. This involved setting up a belongs_to / has_many relationship in Rails. Sites are dependent on Trips.

Anytime a trip is deleted all of the sites are deleted from the database too. This functionality appears in the frontend app. 

CRUD

The user has the ability to create, read, update and delete (CRUD) all trips and sites. These were coordinated by writing fetch requests on the frontend, which through the use of the package Thunk, was able to access the database, make the appropriate updates, send the information with JSON via the Rails API and have the frontend manage that information and make appropriate changes in the Redux store.


Routes

Trip Planner creates routes in the browser utilizing <Router> from  the package react-douter-dom.  I created a home route, a *trips* route to display all created trips, and a make a *trip* route that does just that. The ability to create a site is within each trip itself. All of the above mentioned follow RESTful routing formats with trip and site views following this convention as well. For example, a new trip is shown at *trips/1* and so on

DB

The database was connected via a Rails API. It is a SQLite3 database, as is the standard for Rails apps. The database receives information from the React frontend via fetch and then uses the standard HTTP requests to make changes through the appropriate controller. For instance, if the frontend sends a JSON object as a POST request via the fetch method, the Rails controller will access the *create* method in it the trips controller and then create a new trip object with its own unique id in the sqlite3 database. The database will then return that new object and React will take the JSON object back via the Rails API and then dispatch the action ‘*ADDTRIP’* to the* tripsreducer* that will then add this new trip to the trips array housed in the state of the Redux store.

I enjoyed this project and learned how helpful and flexible the React framework is with building powerful applications for the web.

