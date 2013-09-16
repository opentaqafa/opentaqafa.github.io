# How To Deploy Website Generated Using Jekyll To Heroku As Rack App

Instructions below will show how to get the necessary files apart from Jekyll generated website in order to deploy it on Heroku.

## Prerequisite

A website/blog generated using [Jekyll](https://github.com/mojombo/jekyll).

## Instructions

Step 1 :
```bash
cd my_jekyll_website

```
Step 2 :

```bash
Download and place all the above files except README.md as it is inside my_jekyll_website.
These are the important files which tells Heroku to treat the app as Rack app and just sets
it up on Heroku easily.
```

Step 3 :

Add this to you `_config.yaml` file

    exclude:  [ Gemfile, Gemfile.lock, Procfile, vendor, gems]

This prevents Jekyll's test posts from showing up on your blog.

Step 4 :

Run following commands :
```bash
jekyll
heroku create
git push heroku master
```

Step 5 :

Visit your website :
```bash
heroku open
```

## More Information

[Jekyll-BootStrap-Heroku](https://github.com/nblumoe/jekyll-bootstrap-heroku)

