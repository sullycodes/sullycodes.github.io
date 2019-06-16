---
layout: post
title:      "CLI Project"
date:       2019-06-16 14:20:23 +0000
permalink:  cli_project
---


For my CLI project, I decided to create a gem called Massachusetts State Parks. There are 156 state parks in MA. 

The first step was in designing a Scraper class to scrape from the list of parks and then on the 2nd level to scrape info about each individual park. After figuring out how to scrape from the mass.gov state parks site, I needed to create a way to display a list of these parks. So, I developed a Park class that built park objects from the scraped data.

I also created a CLI.rb file that was the interface for the user and contained many methods to display and act on user choices. It is in this CLI file where the list of parks is created and displayed to the user. 

Because 156 parks is a little much to take in all at once, I decided to display only 30 at a time. If the user does not like the choices displayed they can ask for the next 30 and continue this process until the last 36 are displayed. 

The user is also given many opportunities to start over or leave the program.

Overall, I really enjoyed this project and had fun creating something of my own from the skils we have learned thus far.

I am looking forward to creating more programs!

