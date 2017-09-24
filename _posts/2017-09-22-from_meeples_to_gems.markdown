---
layout: post
title:  "From Meeples to Gems"
date:   2017-09-22 15:12:19 -0400
---


What an adventure it has been so far from the basics of Ruby to publishing my own Gem. There were many bumps in the roads, but I excited to have a working gem published. This is my path to creating my first gem -- TopBoardGames!


## How to Start?!?

My first thoughts after reading the project details was "How do I even get started?". For the majority of the lessons, we were given a starting point or some tests we could run to get an idea of what we needed to do.

There was none of this - simply a blank page on the screen.

Luckily there were super helpful videos (and student examples) that had some walkthroughs giving an idea of what this project would look like. I dove into these in the evening and was excited to get started the next day.

## Looking for that special site

I started by looking at a NY hiking site that listed top hikes in the NY area ([hikethehudsonvalley.com](http://www.hikethehudsonvalley.com)). The first page was already setup with a nice table, each table row being a different hike name so this part seemed simple enough. 

On to the hike description page which was definitely going to be a challenge. Every hike detail was simply a paragraph and looked like it would have been difficult to scrape

```
<p>
<strong>Highlights: </strong> 
Panoramic views, beautiful trails, the burning of many, many calories
</p>

<p>
<strong>Distance: </strong>
5.4 miles, loop
</p>
```

I decided to move on and landed on [BoardGameGeek](http://www.boardgamegeek.com), a site that was essentially a database for board games, card games and more!

## Scrape away!

Right off the bat, I had a list of top 100 board games in a nice table format with the rank, name and rating. Each section had a different class, making it easy to scrape the text along with the board game URL.

```
<tr id="row_">		
 <td class="collection_rank" align="center">					
 <td class="collection_thumbnail">
 <td id="CEcell_objectname1" class="collection_objectname">
 <td class="collection_bggrating" align="center">
 ...
</tr>
```


I went on to the check out the boardgame description page to look for more data to scrape. I knew I wanted for users to be able to select the board game out of a list and be able to get more details. From here there was a ton of information, so I decided I was going to display the weight, playing time, recommended age and a short description of the game. 

![The boardgame description page](https://i.imgur.com/E3h5S4b.png)

All of this looked pretty accessible...until I looked at the source code.

## APIs to the rescue

Now looking at the source code, I realized that this data was not simply text in the HTML code. It looked like it was being populated through the use of JavaScript. I spent some time (possibly too much) digging around seeing what I could extract using Nokogiri. 

There was no way to get this text using Nokogiri, I have to move on. But the only text that could scrape for was the short description that was in a paragraph and that's not what I had envisioned.

But then I remembered that I had seen other sites that use data from BGG and I thought there must be another way. I did some searching and found that BGG offered API and had a handy guide.

The API needed a boardgame id, which I had from the boardgame URL, which allowed me to view the same data from the description page in an XML format. Simple enough!

I still planned on using Nokogiri and after a playing around with the page, I was finally able to extract the data I was looking for.

![Not the nicest...but it works](https://i.imgur.com/hOtHSQj.png)

I didn't have any project files yet, so I saved my code in a TextEdit file. Not the cleanest but worked for keeping track

### Moving On

Now that I knew what data I was scraping for and had my Nokogiri code set, I was ready to move on and actually start building the gem. Throughout this process, I read up on the (long) Nokogiri documentation and learned a ton of methods that made scraping much easier.

I was excited to move forward using what I learned from the walkthrough videos and my own Googling skills. I learned to use the guides and examples as a template, but not a step by step as each person's gem will be different and involve different steps.

I was looking forward to the new challenges that would arise...
Testing
# New HeaderTest
test
