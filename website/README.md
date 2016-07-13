# Guide to the HackProject.org Documentation

HackProject.org's documentation was built using the following components:

* [Hugo](http://gohugo.io) --- Static site generator
* [GulpJS](http://gulpjs.com) --- Build tool for static assets
* [Twitter Bootstrap](http://getbootstrap.com) --- CSS and JavaScript

## Setup

Fork project from GitHub web to your own account.
https://github.com/lewiskan/hackprojectorg

Clone your own project (e.g., $ git clone https://github.com/${YOUR-GIT-NAME}/hackprojectorg)

```bash
$ git clone https://github.com/${YOUR-GIT-NAME}/hackprojectorg
$ cd hackprojectorg
```

Set upstream git path
```bash
$ git remote -v
$ git remote add upstream https://github.com/lewiskan/hackprojectorg.git
$ git fetch upstream
$ git merge upstream/master
```
This sets upstream path to origin.  NOTE: hackproject site is hosted on branch gh-pages, see publishing section when ready to publish.  

Remember to fetch upstream and merge to upstream/gh-pages when ready to publish!

Create your local git gh-pages branch.
```bash
$ git checkout -b gh-pages
```
This version should be merged to upstream/gh-pages
```bash
$ git fetch upstream
$ git merge upstream/master
```

If you have [Homebrew](http://brew.sh) and [npm](https://www.npmjs.com)
installed:

```bash
$ cd /path/to/hackprojectorg/website
$ make setup
```

This will install Hugo, Gulp, and all necessary Gulp plugins.

## Running the Docs Locally

```bash
$ hugo server --watch
```

This will the docs locally on `localhost` port 1313.

## Working with Static Assets

To build a full static asset distribution (CSS, JavaScript, fonts, and images):

```bash
$ gulp build
```

To work on assets in "watch" mode:

```bash
$ gulp dev
```

Publishing - make sure you are on branch gh-pages
```bash
$ git checkout gh-pages
```
fetch upstream and merge changes to local branch.
```bash
$ git fetch upstream
$ git merge upstream/gh-pages
```

View changes (cd to /website directory):
```bash
$ hugo server --watch
```
update changes (add video, etc.)

When ready to merge (publish) to hackproject.org, run the following:
```bash
$ gulp build
```

```bash
$ hugo
```
(builds public directory)

git commit, then push to branch 'gh-pages'
```bash
$ git add ${YOUR FILES}
$ git commit -m '${YOUR COMMIT MESSAGE}'
$ git push origin gh-pages 
```
this will publish 

