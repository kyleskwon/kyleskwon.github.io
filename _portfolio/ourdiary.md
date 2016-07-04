---
layout: post
title: OurDiary
thumbnail-path: "img/ourdiary1.JPG"
short-description: Private memory and plan storage for couples (RoR)

---

{:.center} 
## Summary

OurDiary helps couples remember an array of experiences, make definite plans for the short term, and dream about your bucket list. It accomplishes this in a private setting, only for partners to access. By taking a walk down memory lane together, partners will experience nostalgia from the past as well as excitement for their future!

- Wrote user stories with technical requirements and tracked bug reports on Github Issues 
- Integrated Google Maps API to display customized map from user input
- Used Ruby gems for user authentication, roles, testing, payments, location, calendar, and images

*The following screenshots are from the original version of OurDiary. I am currently refactoring the frontend, so I will update the images when it's complete.

<br>

{:.center-image}
![]({{ site.baseurl }}/img/ourdiary1.JPG)

<br>

{:.center} 
## Context

"Babe, do you remember what we did for our anniversary five years ago?" 

"Of course I do!" 

(Enter mild panic mode)

Unfortunately, I come across this situation from time to time. I have so many awesome memories with my girlfriend that, literally, it can be a lot to keep track of over time. I mean, we've been together for nearly 7 years. How can I remember everything we've done since college by date?

There are several mobile applications on the market, like Couple and Between, but I wanted to build an app without all the bells and whistles. As the saying goes, sometimes, less is more. I'll explain this philosophy as I go along.

{:.center} 
## Problem

Most of us don't have picture perfect memory. 

Admittingly, some partners have difficulty remembering what they did every birthday, holiday, etc.

Personally, I still use Facebook, but I hardly post on it because I like keeping some life events private. I wanted a place for us to be able to remember the experiences we had with family and friends in all kinds of places. 

{:.center} 
## Solution

To go back to my philosophy on building a minimal application, I will start off with my idea to attach only a single photo to each memory. This immediately popped in my mind because I get tired of seeing an overload of images online when friends post pictures. Sometimes, I just want to look at a single photograph and reflect on that experience while repainting the image in my mind. 

Before I created the app, I brainstormed my ideas with my mentor, Chris. We defined technical requirements and I wrote user stories. We agreed that there were a ton of Ruby gems that I could install to leverage other developers work and make OurDiary simply awesome.

As I created the Rails app and got things up and running quickly with a technique called scaffolding, I tracked bug issues with Github for Chris and I to discuss and tackle during our meetings. For the most part, I was able to implement the user stories on my own by reading documentation and using my knowledge from my coursework with the Bloc backend web developer course. 

{:.center-image}
![]({{ site.baseurl }}/img/ourdiary2.JPG)

{:.center-image}
![]({{ site.baseurl }}/img/ourdiary3.JPG)

{:.center-image}
![]({{ site.baseurl }}/img/ourdiary4.JPG)

{:.center-image}
![]({{ site.baseurl }}/img/ourdiary5.JPG)

{:.center-image}
![]({{ site.baseurl }}/img/ourdiary6.JPG)


{:.center} 
## Technology and Implementation

The following are the Ruby gems that brought OurDiary to its current state. They were implemented in the following order.

> - Devise for user authentication
> - Pundit for user roles
> - Rspec for testing
> - Stripe for payments
> - Geocoder for location
> - Fullcalendar for dates
> - Paperclip for images


We also used the Google Maps API (to show a visual layout of where events take place), Bootstrap (I hadn't taken the frontend web developer course with Bloc yet, so this was very useful for clean styling), AWS S3 (for storing images), and Heroku (to deploy the app).
