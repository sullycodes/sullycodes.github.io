---
layout: post
title:      "Sinatra Project"
date:       2019-08-27 15:46:44 +0000
permalink:  sinatra_project
---


For my Sinatra project, I chose to create an app called PeakGeek that keeps track of the peaks that a person climbs. Within this app I used a number of Ruby practices including CRUD (Create, Read, Update and Destroy) and REST (Representational State Transfer.)

CRUD is the practice of allowing a user to CREATE a new object (for example, a peak climbed), being able to READ that item ( a page displaying the peak information and user experience), the ability to UPDATE a peak (change a peak's information if necessary) and to DELETE that Peak from the list (maybe if one was written in error).

REST has to do with conventional URLs. REST was created so that there exists uniformity for website urls. For example, if a user wants to see their peaks, the url would be peakgeek.com/peaks. This is an index of all peaks. If my site had blog posts, instead of peaks, it would be written as myblog.com/posts.

Many of the other urls then piggyback on the peaks url. peaks/new, peaks/5, peaks,/7/edit, etc.

I also employed the use of helper methods for repetitive code. For example, logged_in? is used to ensure that their is a session with a user id . Connected to this method is authenticate which is used to ensure that a user is logged in and if they are not they are redirected to the login page. These methods help cut down on extraneous code used multiple times in the app.

I also added authorization as a way to protect another users peaks from being viewed or altered. To implement this the code checks to see if the current user id matches the  owner_id of the peak. If it does then they are allowed to continue, if not then an unatuthorized page is displayed and the user must return to their own peaks page.

I also incorporated error messages when users login incorrectly and they do when they do not complete forms. They cannot login, signup or edit unless they have done so properly. Red error messages show on the page.

I had some trouble with my local environment. For a while shotgun was not working properly, so I switched to using thin. Then, for some reason that began to not work properly. Eventualliy, after getting help and uninstalling and reinstalling gems and changing versions things became functional again. This was far and away the most difficult part of this project.

I learned a great deal about how to approach a Sinatra project and I also found it a vto be ery helpful reinforcement of the knowledge and skills I have acquired in Ruby coding and implementing Sinatra apps.

