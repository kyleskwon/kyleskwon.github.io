---
layout: post
title: SeoulTidbits (previously Yappit)
thumbnail-path: "img/yappit1.JPG"
short-description: Insider tips for small businesses in Korea (RoR)

---

{:.center} 
Want to find out more about a small business in Korea, but can't be bothered with long reviews? 

{:.center} 
SeoulTidbits is the simplified version of Yelp, saving you time and headache. 

<br>

{:.center} 
## Context

Initially, SeoulTidbits was named Yappit because it was a Reddit replica. It was my first Rails app that I built with my mentor. My friend and I wanted to transform it into something useful for family, friends, fellow expats, and local citizens living in Seoul. 

First I will describe how I built Yappit with my mentor, Chris. Then, I will explain how I am transforming it into SeoulTidbits with my business partner, Stephen.

The screenshots of SeoulTidbits will be updated once Stephen and I work out the UI/UX. We are currently working on it so he can pitch the idea to one of his contacts. In the meantime, the screenshots of Yappit will provide a glimpse of the functionality of the application. Keep in mind, I didn't know much about frontend development, so the design is minimal. My focus was to get to know the Rails framework and ensure smooth functionality. 

{:.center-image}
![]({{ site.baseurl }}/img/yappit1.JPG)

<br>

{:.center} 
## Problem

{:.center} 
Korea doesn't use Yelp. Looking up restaurants on blogs is tedious.

<br>

{:.center} 
## Solution

{:.center} 
Provide the best tidbits about a small business with an up-voting system, similar to Reddit. 

<br>

{:.center}
### Process

To begin, I created and deployed my Rails app using Heroku. Along the way, I learned a lot of caveats about the MVC architecture. I read about static pages, testing, HTML, CSS, models, object relational mapping, and seeding data. 

There is one topic I will highlight before moving on. Testing.

Throughout the process, we used test driven development (TDD). It is a best practice that serves to narrow the focus of the developers code. By programming to pass specific tests, it reduces the chances of introducing errors. It's also easier to pinpoint a bug because new tests aren't written until all tests pass. TDD involves three steps; Red, Green, Refactor. The first step is to write a test that fails in terms of production functionality. The second step is to write the production functionality to make the test pass. Finally, the code is refactored to follow the DRY principle (don't repeat yourself). In other words, this means writing code that is more succinct. 

Next, Chris and I dove into CRUD operations; it stands for create, read, update, and destroy. For resourceful routing, they align with the controller HTTP verbs POST, GET, PUT/PATCH, and DELETE respectively. We planned to apply CRUD actions to topics and posts, similar to how Reddit has subreddits. Also, I associated topics with posts. 

{:.center-image}
![]({{ site.baseurl }}/img/yappit2.JPG)

Then, I learned about validations and authentication. 

Validations are meant to ensure that data meets certain criteria before they are added as attributes. It prevents unwanted data, or lack of data, from being added to the database. For example, they can be checked for character length, special characters, or simply presence. Authentication deals with the user model, signing up for an account, and signing in. Devise is a Ruby gem that I installed to make the process more succinct. At that point, it made sense to associate users with posts. Additionally, I learned about authorization, which designated user roles and access rights. The Pundit Ruby gem helped with this aspect of the application. 

After that, we worked on 

comments, which were associated with posts 

labels, which were polymorphically associated with topics and posts

{:.center-image}
![]({{ site.baseurl }}/img/yappit4.JPG)

voting, which ranked posts with a time-decay algorithm

{:.center-image}
![]({{ site.baseurl }}/img/yappit3.JPG)

favorites, which followed up by sending an email to the user who created the post

{:.center-image}
![]({{ site.baseurl }}/img/yappit5.JPG)

user profiles, which listed their contributions

private topics, which restricted access from users who were not signed in

ajax, which created and deletes comments without reloading the page

and 

building an API, which involved retrieving and sending data


<br>

{:.center} 
## Technology and Implementation

Ruby on Rails, Bootstrap, Heroku
<br>

> Ruby gems
>
> - Rspec for testing
> - Devise for users
> - Pundit for user roles