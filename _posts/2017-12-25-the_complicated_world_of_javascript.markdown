---
layout: post
title:      "The complicated world of Javascript "
date:       2017-12-25 22:25:57 -0500
permalink:  the_complicated_world_of_javascript
---


Coming from Ruby, Javascript seems like it is more complicated than it should. If Ruby can be so elegant, why aren't all languages like this?

Javascript seems like it was made to confuse programmers to keep us on our toes! Despite this, its highly used and it necessary to do fancy client-side stuff so we will have to dive right in. 

## The preparation

Going through the course, it seems like we went head first into learning JS, which may be good for those who have had some experience with programming in the past. I found my self re-reading the same text (which may also be a result of long days), as I kept expecting it do the same as Ruby. As I progressed, I found myself constantly comparing it to Ruby, thinking why would someone ever use this when Ruby exists. JS sure seemed like a language built in 10 days.

Nonetheless, I kept learning and slowly began understanding certain aspects and how developers use JS. Given that JS is popular, there must be a reason why devs use it daily. Especially when it is built into all browsers.

While I know I only scratched the surface of Javascript, it increased my curiosity of what it can do and am excited to keep learning on my own. 

For now, I can take what I learn and move to see how it could be used to the all-powerful Rails. 

# Rails + JS refactor

Right off the bat, I saw so many changes I could make using Javascript while I reviewed my previous Rails. Simple things like form submissions could be done on the fly with the use of AJAX and automatically update the DOM.

This is the same behavior I expected of most of the web apps I used on a daily basis. I could see how my Rail app could start behaving like the other web apps out there and was excited to start tinkering. 

I started with the simple create form which I planned to hijack the form submission and instead use AJAX to POST to my Rails route and return the newly created instance data. With this instance data, I could append my list of preexisting instances via the DOM. I could do this without having to redirect or reload the page. Such amazing AJAX magic.

My next task was to update my report filter button to update the page based on the dates selected and when the form was submitted. 

Once again, I hijacked the form submission event and used an AJAX GET request to return a list of object instances that had a date that matched the dates selected. This querying was still being done by my Model/Controller.

## Conclusion

While I was able to implement some simple AJAX calls into my Rails app using JS, I know I only scratched the surface and I am excited to keep researching and learning more way I can implement JS into my apps in the future. 
