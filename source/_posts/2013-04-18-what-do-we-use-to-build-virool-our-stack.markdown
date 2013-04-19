---
layout: post
title: "What do we use to build Virool - Our Stacks"
date: 2013-04-18 18:04
comments: true
categories: General
author: Vlad Gurgov
---
This is what we use to make Virool the best video promotion site ever!
## Web Stack
We use Ruby on Rails and Ruby for most of the web stuff. Some of the tracking services use Sinatra, another use just plain nginx and write to csv logs.
Our API is mostly migrated to Scala. It started as Ruby as well, but we quickly bumped into memory/GC limitations, not being able to serve more than like 1000 requests per server was a bummer.

Our DB is still good old Postgres. We started with MySQL, made tons on performance improvements for it, but it was still nowhere near what we needed. Making hot updates on our production DB during our rapid development was a huge pain. Switching to Postgres was one of the best decisions we ever made and it immediatelly paid back.

We memcache a lot. All of out API and most of functionality on site comes out of cache, so we touch DB very rarely.

Besides that we user regular tools and frameworks like Bootstrap whenever we can for front end, Sidekiq for backgroud processes, emails etc. Nothing fancy

We host our servers at Rackspace cloud and so far quite happy with their service, although we really miss notice auto-scalling support sometimes.

We store a lot of logs and data on Amazon S3.

## Analytics
Most of us are data geeks, and we are trying not to miss any need analytics tool. At different times we used/use:
Google Analytics, Mixpanel, Kissmetrics, Heap Analytics (this is very cool YC company and service btw. If you you haven't yet give them a try). 

## Developement Process
We are running somewhat our own version of scrum/agile process with weekly sprints. We used to do be-weekly but felt that we can do faster... Most of product management is happening via GitHub issues. We have a new milestone for every week's sprint. We integrated them with HipChat(along with Capistrano) that is great for all communition. Besides than we Skype a lot and use internal development mail-lists.

Our team is distributed between San Francisco and St.Petersburg, Russia so our GitHub repository almost never sleeps. :)

## Office
Most of us live and work in our loved loft in SOMA. Special thanks to:

* Reb Bull and Diet Coke
* Instacart.com for bringing us Red Bull, Coke and some great snacks.
* Grubhub and trycaviar for bringing us delicious meals - something new every day. 
* Exec for bringing us whatever instacart can not bring and allowing us not to leave office during work week
* Zipcar for taking us where ever we want during weekends
* Amazon for bringing us amazing stuff like our in-office gym weights

All of our employees have unlimited access to these services and any other services that will make them more productive


update is coming soon...

Y U NO JOIN us? jobs@virool.com
plz pardon typos and mystakes in this post - we will find more time for bloggin and proof reading  in future, right now we have too many challenging tasks to be finished
