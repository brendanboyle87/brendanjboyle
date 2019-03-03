---
template: post
title: 'How I Got this Site Started in an Hour with Gatsby.js and Netlify '
slug: /posts/starting-a-blog-in-an-hour/
draft: false
date: 2019-03-02T19:50:21.798Z
description: >-
  Short description how I got this blog up and running using Gatsby.js/Netlify
  and a comparison of this stack to my previous experience using Wordpress. 
category: 'Serverless '
tags:
  - Serverless
  - React
  - Gatsby.js
  - Netlify
---
I've owned this domain for years, and for most of that time it's been a parked page. I've made a few attempts at starting a personal site in the past, usually using Wordpress. Wordpress is a great tool that powers millions of sites, but anyone who has used it is probably familiar with the experience below:

### Using Wordpress:

You pick out a webhost that has one click Wordpress deployment (I usually used BlueHost). It costs five dollars a month. You make your admin account. You install Wordpress and you browse free themes for way too long. You get the theme installed. You get it set up as a child theme to make sure you can update the theme without losing any customization. You starting adding the plugins your research says you need (SEO, Commenting, Caching, Security, etc.). You configure all of the plugins and get your About Me/Contact pages ready. After all that is done you still have to worry about storage space on your host, Wordpress updates, what to do if you saw a surge in traffic (okay probably not a huge problem for this blog) and a bunch of other things. 

### Using Gatsby.js and Netlify:

I first heard about [Gatsby.js](https://www.gatsbyjs.org/) and [Netlify](https://www.netlify.com/) on an [episode](https://www.gatsbyjs.org/starters/alxshelepenok/gatsby-starter-lumen/) of Software Engineering Daily. The Gatsby.js site has starter examples that you can get up and running with a few clicks. I picked out the starter [Lumen](https://www.gatsbyjs.org/starters/alxshelepenok/gatsby-starter-lumen/), clicked the Try with Netlify link, and connected my GitHub account. I immediately had a forked repository and a working demo blog at a domain provided by Netlify. A simple A record update had my custom domain pointing at the site.

I was super impressed with the Netlify's built in CI/CD process. If you are working off a feature branch Netlify renders an updated version of the site after each push. Any merge to Master automatically kicks off a deploy to the live site. Within an hour I was able to remove the stock content/images and replace it with my own. 

What really pushed things over the top for me was the inclusion of a built in CMS that required no setup. www.brendanjboyle.com/admin came with the starter out of the box. After signing up as a user of the site through Netlify Identity, I was able to update pages/posts without pushing codes. The updates via the CMS are automatically committed back to my repo. 

I can't say enough great things about this developer experience. The site also loads super fast and looks great on mobile.  The easy setup process has made it way more likely I will follow through and keep posting. I will definitely look at this stack for other sites in the future.
