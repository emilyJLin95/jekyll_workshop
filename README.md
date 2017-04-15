# jekyll Workshop!

[Jekyll](https://jekyllrb.com/) is a static site generator that automates a lot of the site creation progress. It's popular for personal and blogging sites.

## Installation

### Mac
1. Your computer probably comes with Ruby installed! You can verify this with which ruby. If you don't get a path returned, you can easily install ruby with Homebrew. If you plan on doing more serious development with Ruby, you should look into an environment manager, like rbenv, but that's beyond the scope of this workshop.
2. Now you need to be able to install "gems", which are Ruby packages. RubyGems is the Ruby standard for publishing and managing third party libraries. If you installed Ruby with Homebrew or an environment manager, RubyGems should be installed by default. Check if you have gems installed by running the which gem command. If you don't get a path returned, you can download RubyGems here.
3. Last step: it's time to install some gems specific to Jekyll. To do this, simple execute gem install jekyll bundler. If you didn't install Ruby with homebrew or rbenv, you may have to run sudo gem install jekyll bundler.

### Windows
There's a known issue with Ruby on Windows that makes the installation process a little more difficult for first-time users. However, once RubyGems is installed correctly the first time, RubyGems will work just fine. More info can be found [here](http://guides.rubygems.org/ssl-certificate-update/#installing-using-update-packages).
1. Check if you already have Ruby installed. Run your terminal as an administrator (right click when opening and choose, "Run as administrator") and type ```
ruby -v
```
.
  * If that gives you a version number, go to step 2!
  * If not, install Ruby (either by Chocolatey/your preferred Windows package manager or manually).
2. Gem is Ruby’s package manager (similar to NPM for Node). However, due to a bug with windows, in order to get Gem you need to download the gem file manually.
  * Go to [the RubyGems download site](https://rubygems.org/pages/download#formats). Choose the zip version, and unzip it in a easily-reachable directory (like C:\, C:\Documents, etc)
  * cd into the directory where you unzipped it.
  * Run in terminal: ```gem install --local your_directory_path\rubygems-update-2.6.10.gem ```, replacing ```your_directory_path``` with the directory you chose. For example, my command says, ```C:\>gem install --local C:\rubygems-update-2.6.10.gem```
3. Update RubyGems! type in terminal, ```update_rubygems```.
4. To make sure the gem installed correctly, type ```gem --version```.
  * If that gives you a version number, great! Go to step 5. :smile:
5. The rubyUpdate gem can be safely uninstalled. Type ```gem uninstall rubygems-update -x```.  

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
