# jekyll_workshop

# Installation
## Mac
1. Your computer probably comes with Ruby installed! You can verify this with `which ruby`. If you don't get a path returned, you can easily install ruby with Homebrew. If you plan on doing more serious development with Ruby, you should look into an environment manager, like [rbenv](https://github.com/rbenv/rbenv), but that's beyond the scope of this workshop.
2. Now you need to be able to install "gems", which are Ruby packages. [RubyGems](https://github.com/rubygems/rubygems) is the Ruby standard for publishing and managing third party libraries. If you installed Ruby with Homebrew or an environment manager, RubyGems should be installed by default. Check if you have gems installed by running the `which gem` command. If you don't get a path returned, you can download RubyGems [here](https://rubygems.org/pages/download/).
3. Last step: it's time to install some gems specific to Jekyll. To do this, simple execute `gem install jekyll bundler`. If you didn't install Ruby with homebrew or rbenv, you may have to run `sudo gem install jekyll bundler`.

# What does the `bundler` gem do?

- Bundler provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.

# Starting a jekyll project

`jekyll new blog`

`cd blog`

## Serving your project on a browser
The command `bundle exec jekyll serve` will run your files on `localhost:4000`
It’s a barebones look right now though- the default `minima` theme
You can now close the server with `ctrl+c`

# Adding a theme
Feel free to use choose your own theme from [JekyllThemes.org](http://jekyllthemes.org/), but we’ll be walking you through how to use the [`whiteglass` theme](https://github.com/yous/whiteglass).

Edit `_config.yml` to use whiteglass theme and its plugins (replace lines 29-31 with the following):


```
theme: jekyll-whiteglass
gems:
  - jekyll-archives
  - jekyll-paginate
  - jekyll-sitemap

permalink: /:year/:month/:day/:title/
paginate_path: /posts/:num/
paginate: 5

jekyll-archives:
  enabled:
    - categories
  layout: category_archives
  permalinks:
    category: /categories/:name/
```

Now, replace line 15 of your `Gemfile` with: `gem "jekyll-whiteglass"`

You can see what other plugins exist at https://jekyllrb.com/docs/plugins/#available-plugins

The theme also comes with some helpful defaults like an about and an archives page. You can add these files to your blog by running:
```
rm index.md
curl -L -O "https://github.com/yous/whiteglass/raw/master/{index.html,about.md,archives.md,feed.xml}"
curl -L --create-dirs -o _data/navigation.yml https://github.com/yous/whiteglass/raw/master/_data/navigation.yml
```

Because you added gems to `_config.yml` and `Gemfile`, you need to install them with `bundle install`

Now you can simply run `bundle exec jekyll serve` and the blog will be available at [http://127.0.0.1:4000](http://127.0.0.1:4000)

# Workshop

Each workshop session will be ~60 minutes on a web technology, tool, framework, or concept. It will consist of both a short presentation as well as a tutorial. The tutorial will be a written online document in the form of a [markdown](https://guides.github.com/features/mastering-markdown/) readme file in a git repo — you can start by forking this very repo. During the tutorial section the class will work in teams of 3 following along with the instructions in the document. The team presenting will answer questions and help the individual teams along.


## Workshop Overview

* [10-15 Minute Intro Presentation](#presentation-section)
* [30 Minute Tutorial](#tutorial-section)
* [5-10 Minute Wrap-Up Discussion](#wrap-up-discussion-section)

## Teams

Teams of ~5 will be formed around dates and a set of potential topics. Your and your team may chose 1 or 2 technologies from the list or may suggest alternative related technologies/topics.

## Setup

If your tutorial requires any lengthy download or install procedures please let the class know at least 2 days in advance.

## Details


### Presentation Section

~(10-15 minutes)

* motivate the technology
* show where the technology fits into the web dev process (dev tool, frontend framework, preprocessor, language etc)
* show some use cases
* discuss pros/cons

You may use any presentation technology, although [reveal.js](https://github.com/hakimel/reveal.js) is particularly fitting as an open source javascript library, and supports code blocks. :gem:

### Tutorial Section

(~30 minutes)

Your written tutorial document will be a walkthrough of building something using the specific web technologies.

It should include:

* Overview of what will be attempted
* Any necessary setup steps
* Step by step instructions
* Explanations of the what **and** the why behind each step. Try to include:
  * higher level concepts
  * best practices

Remember to explain any notation you are using.

```javascript
/* and use code blocks for any code! */
```

Use screenshots

:sunglasses: GitHub markdown files [support emoji notation](http://www.emoji-cheat-sheet.com/)

Here's a resource for [github markdown](https://guides.github.com/features/mastering-markdown/).

### Wrap-Up Discussion Section

(~5-10 minutes)

* lead short discussion
* answer questions
* individual teams share results
