---
layout: post
title:  "Creating Quick Project Mockups for Your Portfolio with Placeit.net"
date:   2015-10-25 20:00:00
categories: design portfolio
---
While spending some time today getting my resume up and running on my GitHub user page, I started thinking about ways that I could visually display my projects. One of my first projects for the Udacity Front-End Nanodegree program involved building a resume dynamically with JavaScript. The project section of the resume includes several image objects, or really as many as I would like to include. Since I built the resume before I had any projects to show, I had been using placeholder images.

Now that I have a few projects under my belt -- including this blog -- I decided that it was time for the placeholders to be replaced with the real deal. Here is a fantastic site if you are looking to quickly put together one of those infamous troikas that show your website across devices: desktop, tablet and mobile.

<https://placeit.net/>

It took a while of browsing and using the filter to find devices against a white background, which is what I wanted for my purposes. Otherwise, there are a ton of your typical stock art backgrounds, as well as some really interesting options:

![Place your website in front of The Donald]({{ site.baseurl }}/img/donald-trump-placeit.jpg)

One of my favorite features: placeit.net allows you to grab a screenshot from a URL, so there is no need to manually make your own screenshots and crop them to size.

These are all free to download at a small size (400px x 300px), but some will cost you a bit at higher resolutions. 400x300 was plenty for my purposes. The results aren't too shabby:

## Mockups

### Desktop

![Desktop view](http://laurenfromseattle.github.io/img/noob-notation-desktop-400x300.png)

### Tablet

![Tablet view](http://laurenfromseattle.github.io/img/noob-notation-tablet-400x300.png)

### Mobile

![Mobile view](http://laurenfromseattle.github.io/img/noob-notation-mobile-400x300.png)

---

*As an aside, trying to understand the relationship between the gh-pages and master branches when setting up a project on GitHub has been very challenging for me. I still have not managed to implement this correctly.*

*Everything I've read talks about how it is important to set up an orphan gh-pages branch -- one that shares no history with the master branch. The process involves cloning your repo, emptying it out of all contents, then creating the gh-pages branch. I still do not understand where to go from here.*

*I've reluctantly settled for the temporary solution where I continually push everything from origin to master, then merge master into my local gh-pages, then push again to gh-pages. So, I basically have a gh-pages that mirrors the master, with a lot of extra work in between to get them that way. Good enough for now!*
