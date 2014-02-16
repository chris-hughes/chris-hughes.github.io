---
layout: post
title: Building a game in Phaser
description: "Building a simple game in Phaser"
category: articles
tags: []
comments: true
share: true
---

After deciding that I need to focus on building the game first, I've spent a couple of days researching how best to go about it. Now I want this to be as quick and painless as possible so I immediately began looking for a framework I could use in the hope that the framework would provide a whole bunch of useful out of the box functionality.

It didn't take me long to find <a href="http://phaser.io/" target="_blank">Phaser.io</a>, a javascript HTML5 gaming framework. A quick look through showed me it had many features that I would find very useful (plus some others that looked good but probably wouldn't be necessary, like physics!). Although the documentation is a little convoluted the tutorial was extremely good and the community seemed passionate and ready to assist with any problems, including basic errors which I was bound to make.

I also found <a href="http://www.lessmilk.com/" target="_blank">lessmilk.com</a>, which is a very cool site by Thomas Palef where he is building a new game every week using Phaser. This gave me hope that I could make quick progress with Phaser.

### First game

Now I know I'm aiming to build a board game, but I couldn't resist having a play with Phaser's physics engine, which means gravity! So I decided to build a *very* simple platform style game, which would at least get me familiar with Phaser.

I don't think I'm going to win any awards with this but I've certainly learned a lot about the frustrations of working with image files! The game is fairly basic with the aim being to kill all the (evil?) slugs by jumping on them. It's not really polished but I'm trying to follow my own advice and not worry about that, just post and move on.

<div id="game" style="width:640px; height: 640px;"></div>

### Building the game

Phaser is amazingly simple to get started, it really only took me a couple of days to throw the game together and most of that time was not spent writing endless code. The game took less than 100 lines of code, excluding Phaser itself. Everything on this site (including the site itself) is open source so feel free to <a href="https://github.com/chris-hughes/phaser_fun/" target="_blank">take a look at the game</a> and as usual all comments/tweaks are very welcome.

There were 3 main stages in building the game:

* Creating the world
* Creating the characters
* Defining how the characters interact with the world

#### Creating the world

The world consists of a background and a foreground. I knew I could always just set the background to a plain color but I had no idea how I was going to create an interesting foreground. Design has never been my strong suit and even though I'm more interested in making things that work it is always a bit deflating when you've worked hard to make something impressive and then when you show someone all they comment on is how shit it looks! So I was determined to at least make an effort this time, although I'm the first to admit it's not perfect.

I knew I wasn't going to be able to create anything myself, so off to Google and I find the mecca of game art, <a href="http://opengameart.org/" target="_blank">opengameart.org</a>. This place has all that I need to create my game (and possibly Quoridor too), including graphics and sounds.

Now I've never used any image resources like this before but the concept of a tileset is simple and I quickly find one that I like. Only problem was I didn't really know how to use it! Luckily I found <a href="http://toastedware.com/toasteditor/" target="_blank">toasteditor</a> which allows you to basically 'paint' a level and export is as a csv that Phaser can understand. Now that's pretty handy, especially if I wanted to expand my game to multiple levels. I would simply need to create a csv file for each level and switch between them when needed.

#### Creating the characters

The characters were also found on opengameart, this time in the form of a spritesheet. This time there was no difficulty with using them and it only takes two seconds to set up the animations for walking and climbing. There really wasn't else to it then that.

#### Interactions

Phaser comes into it's own here, setting up gravity takes one line of code! It's then a simple matter of defining which of your level tiles the players collide with. Being lazy I just set all tiles to be solid (except the ladder) which is why you can walk on clouds! There was a tiny bit of effort getting the ladder to work and to be honest it's not perfect.

The final piece was to kill the snail/player, depending on how they collide. In an ideal world I would have animated the brutal killings in some way and definitely done something to end the game when the player died but I don't think I would have learned much from it so I decided to leave it as is.

### Thoughts on Phaser

Having built my simple game I can say that I'm extremely impressed with Phaser. It was really quick to get started and has powerful features that are simple to use, plus it has a lot more functionality that I haven't explored yet. Whilst I enjoyed using it and I think I could build a pretty good Quoridor game using it, I'm going to have to put some further thought into whether this is the right direction to go. It may be quick however I'm a little concerned that it may force me to implement things in a certain way that may cause problems later.

<script type="text/javascript" src="/assets/phaser_fun/js/phaser.min.js"></script>
<script type="text/javascript" src="/assets/phaser_fun/js/game.js"></script>