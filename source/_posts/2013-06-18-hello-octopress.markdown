---
layout: post
title: "Hello Octopress"
date: 2013-06-18 14:58
comments: true
categories: 
---

They say sites with different languages should be separate. They also say the sites should be fast. Well, then my Eng version of the site would be on Octopress.

<!-- more -->

Ok, they've described how to set up a fresh new blog with the Github Pages quite well. But there's no guide on how to make it work after git clone on a new machine.
So here's the answer:

```bash
$ cd ~/my_root_folder/
$ git clone git@github.com:username/username.github.io.git -b source my_blog
$ cd my_blog
$ git clone git@github.com:username/username.github.io.git -b master _deploy
```

And then as usuall, make changes to the files like `rake new["My super awesome new blog entry"]` and:

```bash
# In ~/my_root_folder/my_blog/
$ rake generate
$ rake deploy
# The changes from your _deploy dir goes to the server (committed and pushed)
$ git add .
$ git commit -m "An awesome entry added"
$ git push origin source
```
