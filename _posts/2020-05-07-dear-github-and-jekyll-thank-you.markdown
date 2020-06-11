---
date: 2020-05-07T11:58:02.000Z
layout: post
title: "Dear, Github, Jekyll, and Netlify: Thank You! "
subtitle: How I host my website for free and it's quite easy.
description: How I host my website for free and it's quite easy.
image: /assets/images/post_images/git-jekyll-netlify.png
optimized_image: /assets/images/post_images/git-jekyll-netlify.png
category: Product
tags:
  - Jekyll
  - Github
  - Netlify
  - Blog
author: sarthakgarg
paginate: true
---
**Dear** [Github](https://github.com/about), [Jekyll](https://jekyllrb.com/), and [Netlify](https://www.netlifycms.org/):

If you search, you can find God. Searching for 'how to host a website for free' was far too easy and it was because you all exist. So, thank you!

Thank you for [Github Pages](https://pages.github.com/) which allows us to host websites using a custom domain for free. [Jekyll](https://jekyllrb.com/), you are awesome! The markdown file based themes that you provide are not only lightweight, but also database independent that makes it super easy to configure and manage static sites. And last but not the least, [Netlify](https://www.netlifycms.org/), without you, content management on Github would have been a nightmare. Your Open Source Content Management System, with an easy-to-use user interface, is simply the best.  

Setting up my blog, [iStandpoint](https://sarthakgarg.com/), was an easy 3 step process: **Create**, **Upload**, and **Deploy**

**CREATE** A REPOSITORY IN GITHUB

The excellent documentation on the [Github Help](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site) helped me well in getting started. I created the [iStandpoint](https://github.com/gargsaar/iStandpoint) repository in Github, which now host [my](https://sarthakgarg.com/) blog, and made the repository public, so that I can host my site on Github for free.

For using a custom domain, I had the option to configure the custom domain in Github or Netlify, I chose the [later](https://docs.netlify.com/domains-https/custom-domains/configure-external-dns/). So left the **Custom domain** in Github settings blank.

**UPLOAD** A JEKYLL THEME AND CONFIGURE

On the settings page, in the **GitHub Pages** section, there is an option to **Choose a theme**, but frankly, there are countless other [themes](https://jekyllrb.com/docs/themes/) that are much better. So I chose to use a theme by [Thiago Rossener](https://rossener.com/). I downloaded [Jeklix-template](https://github.com/thiagorossener/jekflix-template) and uploaded all the files in my repository. Next, all I had to do was - edit a few files to make the theme personal.

I followed the template [wiki](https://github.com/thiagorossener/jekflix-template/wiki/settings), and started with **_config.yml** where I updated the #Site Settings, updated [disqus_usename](https://disqus.com/), removed a few items under #Social Media Settings, and updated the [google_analytics](https://analytics.withgoogle.com/) id. Created a [markdown](https://www.markdownguide.org/getting-started/) file for myself in the folder **_authors.** Changed favicon and other icons at assets/img/icons, and blog_image.png at assets/img, and I was ready for adding **_posts**.

![Website_template_cover](/assets/images/post_images/template_cover.png "Website_template_cover")

Again, the [Jekyll documentation](https://jekyllrb.com/docs/) was so good that I could understand the framework and customise the template further.

**DEPLOY** THE SITE IN NETLIFY

There are many [options for deploying the Jekyll site](https://jekyllrb.com/docs/deployment/third-party/) and I would recommend to go with Netlify, they have made a very complex thing like deployment, very simple. I started by creating an account at [Netlify.com](https://www.netlify.com/), and followed [this](https://www.netlify.com/blog/2015/10/28/a-step-by-step-guide-jekyll-3.0-on-netlify/) post to add Git repo in Netlify and configured the repo**.**

![netlify-add-new-site-from-git](/assets/images/post_images/netlify-add-new-site.png "netlify-add-new-site-from-git")

Once the site was built, inside **app.netlify.com**, which is a console to manage the site, I configured [Site Settings](https://docs.netlify.com/) and [Domain Settings](https://docs.netlify.com/domains-https/custom-domains/configure-external-dns/) for the external DNS for a custom domain. 

NetlifyCMS, the interface to create and manage content, was available at **netlify_site_name.netlify_subdomain.app/admin** OR **custom_domain/admin**.

![netlifycms](/assets/images/post_images/netlifycms.png "netlifycms")

And off I go, Hurray! I'M NOW [ALIVE](https://sarthakgarg.com/about_me.html) ON THE INTERNET.

In the end, I want to say that I've nothing against [Wordpress](https://wordpress.org/), [Wix](https://www.wix.com/), and [Weebly](https://www.weebly.com/in) - they are really good platforms for building websites. It's just that they are not free (need to pay for using custom domain), not as fast, and most importantly, they don't give a feel that we own the code. 

So, that's why I chose you all because why to pay a penny for hosting websites elsewhere when we can do it for free!

**Regards,** Fanboy
