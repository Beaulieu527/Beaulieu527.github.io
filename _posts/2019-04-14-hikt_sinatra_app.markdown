---
layout: post
title:      "Hikt sinatra app"
date:       2019-04-14 20:41:36 +0000
permalink:  hikt_sinatra_app
---


For this project, I built a full MVC Sinatra application. this application is for people who love hiking. This app allows  you to do a couple of things.

* Sign up 

* Login/Logout

* View your user profile page showing all of the hikes you have created.

* the hike show page allows you to view all of the information about each hike.

* The show page also allows you to leave reviews on yours and other users hikes but you can only edit and delete the  hikes  you have created.

* The hikes index pages shows every hike created by every user that uses the app 

**Here is a breakdown of how I built my app:**

* I created a new repository in github.

* I created my file structure. I already knew that I needed three models - a user, a hike,  and a review. I also had a pretty good idea of what views I would need.

* Using rake and ActiveRecord, I created my migrations. ActiveRecord makes it possible to map my models to my database tables pretty easily. The only tricky part with this is making sure that my column types and names correspond to what informatin I want to store for my models. I had to do this part a couple of times to get it right.

* I wrote my models, making sure to specify my “has_many” and “belongs_to” relationships between my models.

* I built my routes and views simultaneously. 

* Once complete users that can sign up, log in, and perform CRUD interactions with hikes and  reviews.


I think my biggest take away from this project is the contant need for testing as you code. I found myself often pluggin away in the begining only to have errors on top of errors. this taught me the imtportance of using TUX and Pry to test all my code as i go.
