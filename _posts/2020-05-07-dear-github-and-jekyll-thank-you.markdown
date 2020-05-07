---
date: 2020-05-07T11:58:02.000Z
layout: post
title: "Dear, Github, Jekyll, and Netlify: Thank You! "
subtitle: How I host my website for free, and it is way too easy.
description: How I host my website for free, and it is way too easy.
image: /assets/images/post_images/git-jekyll-netlify.png
optimized_image: /assets/images/post_images/git-jekyll-netlify.png
category: product
tags:
  - web development
  - jekyll
  - github
  - netlify
author: sarthakgarg
paginate: true
---
**Dear** [Github](https://github.com/about), [Jekyll](https://jekyllrb.com/), and [Netlify](https://www.netlifycms.org/):

If you search, you can find God. Searching for 'how to host a website for free' was far too easy, and it was because you all exist. So, thank you!

Thank you for giving us [Github Pages](https://pages.github.com/) which allows us to host websites using custom domain for free. [Jekyll](https://jekyllrb.com/), you are awesome! Your file based framework is not only lightweight, but also database independent that makes it super easy to configure and manage static websites. And last but not the least, [Netlify](https://www.netlifycms.org/), without you, content management would have been a nightmare. Your Open Source Content Management System with an easy-to-use user interface is simply the best.  

Setting up my blog, [iStandpoint](https://sarthakgarg.com/), was an easy 3 step process: **Create**, **Upload**, and **Deploy**

**CREATE** A REPOSITORY IN GITHUB

The excellent documentation on the [Github Help](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site) helped me well in getting started. I created the [iStandpoint](https://github.com/gargsaar/iStandpoint) repository which now host [my](https://sarthakgarg.com/) blog, made it public so that I can host my site on Github for free, and used the custom domain bought at [godaddy.com](https://www.godaddy.com/), my preferred domain name provider because they make domain management so easy. 

**UPLOAD** A JEKYLL THEME AND CONFIGURE

On the settings page, in the **GitHub Pages** section, there is an option to **Choose a theme**, but frankly, there are countless other [themes](https://jekyllrb.com/docs/themes/) that are much better. So I choose to use a theme by [Thiago Rossener](https://rossener.com/). I downloaded [Jeklix-template](https://github.com/thiagorossener/jekflix-template) and uploaded all the files in my repository. Next, all I had to do was - edit a few files to make the theme personal.

I started with **_config.yml** where I updated the #Site Settings, updated [disqus_usename](https://disqus.com/), removed a few items under #Social Media Settings, and updated the [google_analytics](https://analytics.withgoogle.com/) id. Followed by **CNAME** file where I added my custom domain name**.** Created a [markdown](https://www.markdownguide.org/getting-started/) file for myself in the folder **_authors.** Changed favicon and other icons at assets/img/icons, and blog_image.png at assets/img, and I was ready to add **_posts**.

Again, the [Jekyll documentation](https://jekyllrb.com/docs/) was so good that I could understand the framework and customise the template further.

**DEPLOY** THE SITE IN NETLIFY,  AND OFF YOU GO

To be honest, Netlify was a bit tricky at first, but once I got a hang, it was smooth. I began with creating an account at [Netlify.com](https://www.netlify.com/) and added **New site from Git.**

![netlify-add-new-site-from-git](/assets/images/post_images/netlify-add-new-site.png "netlify-add-new-site-from-git")

Inside **app.netlify.com**, which is a console to manage the site and not the CMS, I configured [Site Settings](https://www.netlify.com/blog/2020/04/02/a-step-by-step-guide-jekyll-4.0-on-netlify/) and [Domain Settings](<Configure external DNS for a custom domain>) for configuring the external DNS for a custom domain. 

NetlifyCMS, the interface to create and manage content, was available at **https://netlify_site_name.netlify_subdomain.app/admin**. 

![netlify-domain-settings](/assets/images/post_images/netlify-domain-settings.png "netlify-domain-settings")

For me, at **gargsaar.netlify.app/admin**.

![netlifycms](/assets/images/post_images/netlifycms.png "netlifycms")

In the end, I want to say that I've nothing against [Wordpress](https://wordpress.org/), [Wix](https://www.wix.com/), and [Weebly](https://www.weebly.com/in), and they are equally great for building websites. It's just that they are not free (need to pay for using custom domain), not as fast and secure, and most importantly, don't give a feel that we own the code. So that's why I chose you all, because why to pay a penny for hosting websites elsewhere when we can do it for free, and that too with the best!

**Regards,** Fanboy