---
template: post
title: 'How to Use the Netlify.Toml file with React'
slug: /posts/netlify-toml-with-react/
draft: false
date: 2019-08-11T19:50:21.798Z
description: >-
How to configure a react application for netlify deployment with a netlify.toml file. 
category: 'Netlify'
tags:
  - Serverless
  - React
  - Netlify
---
I use [Netlify](https://netlify.com) to deploy/host this blog and I have started to use it for personal projects as well. I absolutely love it. It is one of the few products where the experience truly feels seamless. It makes CI/CD simple and lets me focus on the task at hand instead of how to get it deployed. 

I am using React for my personal apps. My professional experience has all been with Angular/Typescript and I want to improve my skills with another framework/javascript. Netlify promises the ability to deploy a react app in [30 seconds](https://www.netlify.com/blog/2016/07/22/deploy-react-apps-in-less-than-30-seconds/) and they deliver! The default config works great with the out of the box create-react-app. However, there is a note in this blog post about additional configuration that is needed if your application uses React Router. This is important as use of the router is extremely common. 

When using the router netlify needs to understand what resource to point the default route at. There are two ways of configuring this, a ```_redirects``` file or a ```netlify.toml```. The _redirects method is the most straight forward but I decided to use the .toml file. 

I went for the .toml file because I anticipate having to add other types of configuration in the future. The setup is simple but I did hit one speed bump along the way. I initially only added the redirect configuration to the file and my build started failing. The .toml file overrides all of the build config so you also need to include the build/deployment paths. 

The final file looks like this: 

```
# Settings in the [build] context are global and are applied to all contexts
# unless otherwise overridden by more specific contexts.
[build]
  base    = ""
  publish = "build/"
  command = "yarn build"

[[redirects]]
  from = "/*"
  to = "public/index.html"
  status = 200
```

Pretty simple, as you can see. Hope this posts helps you get your own app off the ground. 

References: 
[Netlify Redirect Doc](https://www.netlify.com/docs/redirects/)
[Netlify Toml File Doc](https://www.netlify.com/docs/netlify-toml-reference/)