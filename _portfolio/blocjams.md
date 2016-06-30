---
layout: post
title: Auditory Angular
thumbnail-path: "img/blocjams4.png"
short-description: A Spotify replica for streaming music online.

---

{:.center} 
### Auditory Angular is an online music streaming service.

{:.center-image}
![]({{ site.baseurl }}/img/blocjams1.png)

{:.center} 
#### Technology and Implementation

{:.center}
Auditory is a web application built with AngularJS, Firebase, Grunt, and deployed with [Heroku](auditory-angular.herokuapp.com). It was refactored after originally being written with Javascript, jQuery and DOM scripting. 

<br>

{:.center} 
### Context

When Auditory was first created, I started by building out the basic HTML structure with Bootstrap for CSS. On the landing page, the hero container holds the selling points (see below). External stylesheets such as Google Fonts, Ionicons, and Normalize were included in the index.html file. For CSS selectors, such as classes, the style properties and values were written in the main.css file. 

One of my favorite pseudo-class selectors is the <strong>[:hover](http://www.w3schools.com/cssref/sel_hover.asp)</strong> selector. By changing the font color when a cursor mouses over the element, it brings a sense of liveliness to the interface. 

For responsiveness, I added a viewport tag to properly render the HTML and CSS for devices, that way the page scales to fit the width. Next, I added <strong>[media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)</strong> for <strong>[responsive breakpoints](https://developers.google.com/web/fundamentals/design-and-ui/responsive/fundamentals/how-to-choose-breakpoints?hl=en)</strong>, which correspond to the width of the device's screen. In the media queries, I adjusted the grid system to simplify the division and display of information. This divided elements within a container into full-width, halves, thirds, and fourths. 

{:.center-image}
![]({{ site.baseurl }}/img/blocjams2.png)

Using DOM scripting, I was able animate the selling points using events. By calling .getBoundingClientRect() I was able to measure the distance from top of the selling points to the top of the viewport/window. I also learned about the window.innerHeight property to decide when to trigger the animation. Once the user scrolled 200 pixels into the .selling-points element, I initiated the animation. 

After working on the landing page, I built out the collection and album views (see below).

{:.center-image}
![]({{ site.baseurl }}/img/blocjams3.png)

{:.center-image}
![]({{ site.baseurl }}/img/blocjams4.png)


{:.center} 
## Problem

{:.center}   
What problem?

{:.center} 
## Solution

{:.center} 
Streaming music instantly.






