---
layout: post
title: "Up and Running on Firefox OS"
description: "How to get your first Firefox OS application started"
category:
tags: [template, simulator, beginners]
---
{% include JB/setup %}

Before starting development work on a Firefox OS application (or any application), it's good to get a feel for the platform and the development methodologies used. So I'm going to walk through how I got my first application stood up and working in the simulator.

0. Prerequisites

	I'm using a Mac OS X, but all these intstructions should work on any \*NIX machine. You'll need the firefox browser, git, and NodeJS installed. 

1. Simulator

	While the app itself is a web page, it's nice to see it running on FFOS, even if it's just a simulator. First, make sure you're using the [Firefox web browser](http://www.mozilla.org/en-US/firefox/new/). The simulator is a browser plugin that only works in Firefox (for obvious reasons). Go to the [download page](https://addons.mozilla.org/En-us/firefox/addon/firefox-os-simulator/) for the simulator, and install it by clicking the appropriately named button. Follow the instructions. Congrats, you are now running the simulator.

2. Get the Application Template

	I used a template provided by github user [coymo](https://github.com/comoyo) to get up faster. While there are several templates available, including several provided by Mozilla, the one i'm using provides a sensible set of defaults, and demonstrates common UX patterns, using RequireJS and AngularJS in your app and using NodeJS and Grunt in your development flow. To do this, we have to create a new clone using git, pull in the submodules and dependancies, and then start the development server. Below is my run, with git and npm's stdout removed for brevity: 

	{% gist 5570335 %}
	
	The instructions for do this are available at the [ffos-list-detail repo](https://github.com/comoyo/ffos-list-detail).

3. Load in Simulator

	Now that we have the app source and it's running in a local server, we simply have to load it in the simulator. The app provides a manifest.json (I'll discuss that in later posts), so we can point the simulator at it. In firefox, go to the Tools > Web Developer > Firefox OS Simulator. This will take you to the plugin page, and in the empty text box, enter "http://localhost:8081/manifest.webapp" and click Add URL. This lets the simulator know where your app is. Click the stopped toggle if your simulator isn't running, and then click Open Location on the Simulator controller webpage. Congrats, your webapp is now live on the simulator. Play around with the simulator, get a feel for phone, and then open the app and see what functionaility is available. This will help you understand what's going on when you look at the code.

Now that we have an app running, we have to understand what's it's doing. Look for the next post.

