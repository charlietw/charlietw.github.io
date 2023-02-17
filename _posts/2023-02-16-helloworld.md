---
layout: post
title: "Blog setup"
image:  /assets/banner.jpg


---

## Hello, world!

### Background

Setting up a personal blog has been on my to-do list for quite a while, and an opportunity presented itself where I had some spare time which came up in between projects at work. 

I had several requirements to consider before I even thought about what I would actually blog about:
- I needed it to functional and presentable, but also want to write as little HTML/CSS as possible. Frontend work just doesn't do it for me.
- I don't want to maintain any infrastructure. I do enough infrastructure management at work and for my home automation setup, so therefore it needs to be serverless.
- I want to be able to write posts on my local machine, version control it, and for it to automatically update the 'live' blog when I push to github. 

### Github pages

I looked at various hosting options, the most tempting of which was [hosting it on an S3 bucket](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html), the advantages of which would be scalability, ease of setup, and frankly, cool-ness. However, even though I wouldn't be managing any infrastructure, I would still need to manage the bucket and the Terraform defining the bucket. 

I was aware of Github pages, and settled on using that, because it is about as hands-off as it is possible to be. When combined with [Jekyll](https://jekyllrb.com/), the level of automation you get really is impressive. The only Terraform I needed to write was to manage the route53 domain so that users can access the blog at this URL rather than the default Github pages one. 

### Theme

The default theme for Jekyll, 'minima', is actually pretty nice, but I wanted a bit more customisation, and after some research came across the ['basically basic'](https://github.com/mmistakes/jekyll-theme-basically-basic) theme, which seemed to fit the 'functional and presentable' requirement, it was easy to set up, and had plenty of options for further customisation if I needed (unlikely if it means I have to write HTML/CSS...).

