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

<div id="game" style="width:640px; height: 640px; background-color:red;"></div>