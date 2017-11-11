---
layout: post
title:      "Comicbooks Galore!"
date:       2017-11-11 05:09:51 +0000
permalink:  comicbooks_galore
---


I started putting this project off due to the amount of time it took my to just setup my previous CLI project. After reviewing some of videos and previous labs, I began mimicing the inital setup that had been done for those. 

As a continued to follow the videos and labs, I noticed that is was much easier to set up a Sinatra app compare to the CLI. Not sure if this was because I submitted the CLI to rubygems but Sinatra already seemed easier.

It seems like for me, the biggest hurdle for these projects is getting started. Once I get a good flow going, I can work for hours before I realize I should probably get something to eat to fuel my brain power. 

Once I got the basics of the Sinatra app up, Gemfile, Rakefile and migrations, I was ready to move foward. 


# The Idea
Once I had my basics setup, it was time to start thinking what my Sinatra app would actually do. I decided on comicbooks database as I was recently began reading the original Dragon Ball manga, I decided it was relevant to my current hobby. 

It would make a pretty easy transition when setting up associations. I figured Authors could have many Comicbooks, and Comicbooks would belong to one Author.

# The Implmentation
Once I had my idea, I began setting up my database by creating my migration file via the rake command which makes everything much easier :)

I setup my tables and columns in the migration files and ran rake db:migrate to create the tables in my migration files. Finally I was ready to create my routes.

Setting up the routes in the my controller files came like second nature as I had recently done the previously labs which gave me really good practive of the RESTful routes that I used. 

Lastly, I setup my erb files which I enchanced by add Bootstrap to my layout.erb file to give my app a bit more flair.

# Moving On
Setting up this project was a blast, I most likely spent way too much time playing around with the Bootstrap CSS to get my app nice and pretty, but it was worth it in the end. I learnt alot, ActiveRecord makes things so much easier and can't wait to foward to the next section. 

