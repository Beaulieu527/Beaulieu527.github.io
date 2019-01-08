---
layout: post
title:      "MA BREWERIES CLI"
date:       2019-01-07 21:55:10 -0500
permalink:  ma_breweries_cli
---


So here we are all of our hard work these past couples of months have to lead to this, the first major project of the Software engineering course. I must say this project for me was a lot of work with many trials. 

The biggest issue I had was pure procrastination, this is something I sometimes struggle within all aspects of life though. The first day i was supposed to start the project I looked at the project guidelines and felt completely overwhelmed, I had no idea where to start or what to do I felt as if it was out of reach for my current skill level, with those feelings I stepped away from my computer for the rest of the day I sat and pondered what it was I really needed to do.

The next day I came back to re-read the project outline and started to try and break it down step by step. The first me was to read everything step for me was to find out what I wanted to base my CLI on. I chose the Open Brewery DB API which is basically just a large database of all the breweries in the country, I chose this because well obviously I love beer and need to find it as fast as possible. Once i picked what I wanted to base my project on I needed to figure out what I wanted it to do, it was pretty obvious at this point. I wanted to be able to search the breweries by Name, Street Name, City, and Brewery type. Great now I know what I wanted this CLI to do now I just had to figure out how to code it.  

The biggest challenge coding my project was trying to figure out how to parse all of the pages of the database together. Unfortunatley the api i chose did not have an endpoint that would show all the breweries in a list, it was paginated into hundred of pages containing 50 breweries on each page, I had to cut this down and make it more managable so i chose to only parse breweries in Massachusetts. From that point I knew I had to loop through the page numbers to parse each page to get the information to create my attribute accessors, but I didn't want to hardcode it  like this example:

```
def initialize
    i = 1
    while i <= 4
      page = open("https://api.openbrewerydb.org/breweries?by_state=Massachusetts&per_page=50&page=#{i}")
      i+=1
      breweries = JSON.parse(page.read)
        breweries.each do |attributes_hash|
          MaBreweries::BREWERY.new(attributes_hash)
        end
    end
  end
```



This  would just loop through each page until  the loop hit 4 and would exit.

I wanted  the function to be fluid so that if new breweries are ever added my application would be able to load them. to be able to do this I came up with this method:

```
def initialize
boolean = true
i = 1
while boolean do
page = open("https://api.openbrewerydb.org/breweries?by_state=Massachusetts&per_page=50&page=#{i}")
i+=1
breweries = JSON.parse(page.read)
if breweries.count == 0
boolean = false
else
breweries.each do |attributes_hash|
          MaBreweries::BREWERY.new(attributes_hash)
        end
      end
    end
  end
```

By setting the boolean to true i would loop through each page until I reached an empty array which would then switch boolean to false and exit the while loop.

Once I figured out how to parse all my pages together I was off and running coding all of my classes and search methods. There were still more trials along the way but for me that was the biggest hurdle.





