---
layout: post
title: Auditory Angular
thumbnail-path: "img/auditory4.png"
short-description: A Spotify replica for streaming music online.

---

{:.center} 
### Auditory Angular is an online music streaming service.

{:.center-image}
![]({{ site.baseurl }}/img/auditory1.png)

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
![]({{ site.baseurl }}/img/auditory2.png)

Using DOM scripting, I animated the selling points using events. By calling .getBoundingClientRect() I was able to measure the distance from top of the selling points to the top of the viewport/window. I also learned about the window.innerHeight property to decide when to trigger the animation. Once the user scrolled 200 pixels into the .selling-points element, I initiated the animation. 

After working on the landing page, I built out the collection and album views (see below).

{:.center-image}
![]({{ site.baseurl }}/img/auditory3.png)

{:.center-image}
![]({{ site.baseurl }}/img/auditory4.png)

<br>

{:.center}
### Refactoring with AngularJS

Eager to learn a Javascript framework, I created a new repository in Github to get started. Next, I migrated the audio and image assets plus the CSS stylesheets to the new project. New script files were added to reference the Angular script file. After that, I bootstrapped the application I was off to the races. 

From there, I browsed the documentation to learn about modules, controllers, services and more directives. Along the way, I wrote my own documentation for attributes, functions and methods.

With controllers, I created separate states that corresponded to the landing, collection and album views, which are referred to as templates in Angular. First, I learned about the ui-router to utilize its built in directives. In the index.html file, the ui-view directive shows the contents of the template when the user navigates to the route. The ui-sref directive is used to trigger a state. 

For services, functions were written to be shared across different components. For example, the Fixtures service held album data including the title, artist, label, year, albumArtUrl, and songs in an array of objects. This service was injected into the controllers to be used in albums and the collection of albums. 



<!--
{:.center} 
## Problem

{:.center}   
What problem?

{:.center} 
## Solution

{:.center} 
Streaming music instantly.
-->






