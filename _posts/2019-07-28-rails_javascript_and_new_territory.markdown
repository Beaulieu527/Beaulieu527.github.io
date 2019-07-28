---
layout: post
title:      "Rails JavaScript & new territory."
date:       2019-07-28 19:53:17 -0400
permalink:  rails_javascript_and_new_territory
---


For my fourth project in the flatiron course, is a continuation of my Rails project Hikt. To complete this project  I had to take my current project and add Javascript and Jquery to it to make parts of the application load asynchronously through Ajax  {"Asynchronous JavaScript and XML"}. Hikt is for people who love the outdoors and hiking and want to keep track of which hiking trails they have “Hikt”. With the use of this app, a user can create an account either by filling out a Sign Up for or by signing up with Facebook. Once they are signed in, they can browse Hiking trails that other users have added to the database and also leave reviews. If they would like, they can create a Hike by adding a picture, location summary and length.

Upon starting this project I thought it was going to be a lot easier and more straight forward. as I progressed the idea of converting my app into a single page was brought up. Did I know how I was going to do it? NO! But challenge accepted! I spent the next few nights after work trying to figure out what my app would now look like and how I would be able to show all my information on one page simplistically. That's when I came up with the idea loading my index page upon login and using Bootstrap modals as my show page.  As you open each modal all of the hike information and reviews left by users would be collected from my backend Rails API and parsed directly into the "Show" modal through a Fetch Get request. once loaded there is also a form on the bottom to leave new reviews which would also load asynchronously to the show page without a refresh. 

I ran into many obstacles throughout this project from trying to parse all of the correct information to the show modal to passing the correct IDs in my form. It seemed like everything with this project was a struggle, But alas I was able to persevere.
