---
layout: page
title: Environment Setup
section: Environment & Source Control
---

Setting up your environment can be difficult when you're first starting with Ruby and Rails. To make matters worse, there is a lot of outdated and wrong documentation out there on the web.

Here's a concise guide to the current best practices.

### Goals

Generally speaking, we want to get the following installed:

* A text editor
* Ruby 1.9.2
* Rails 3.2.0
* Git

### Text Editor

If you've programmed in other languages before, you might ask which IDE Rubyists prefer. The answer is 'none, they use text editors.' Ruby IDEs do exist, but the overwhelming majority of Rubyists use a text editor and a command-line prompt.

We recommend [Sublime Text 2](http://www.sublimetext.com/2) for beginning Rubyists. It works the same across Mac, Windows, and Linux, and has an unlimited trial.

If that's not your cup of tea, try one of these other editors:

* [Redcar](http://redcareditor.com/) is an editor written in Ruby itself. It runs on all platforms.
* [Notepad++](http://notepad-plus-plus.org/) for Windows.
* [BBEdit](http://www.barebones.com/products/bbedit/index.html?utm_source=df&utm_medium=banner&utm_campaign=bbedit) or [Textmate](http://macromates.com/) for Mac OS.
* [RubyMine IDE](http://www.jetbrains.com/ruby/) for all platforms.

The most popular editor amongst professional Rubyists is [vim](http://www.vim.org/), but learning how to use it is almost as hard as learning programming itself. You shouldn't use it unless you want to invest the time to learn it, which is a whole separate endeavor.


### Mac OS

Mac OS is the most popular platform for Ruby and Rails developers. To have a properly setup dev machine you want the following:

* XCode 4
  * XCode is necessary to have all the development headers and compilers available on your system
  * If you have an OS X installation disc, the XCode Installer package appears in the disc's Optional Installs folder
  * Double-click the .mpkg file to open the installer and begin the installation process
  * Otherwise, download it from the App Store:  http://itunes.apple.com/us/app/xcode/id422352214?mt=12
* Homebrew
  * Homebrew is a package management system that makes it super easy to install hundreds of open source projects and compile them from source for maximum performance on your machine. 
  * Find download and installation instructions at http://mxcl.github.com/homebrew/
* Git
  * Git is the version control system of choice in the Ruby community
  * Once Homebrew is installed, run `brew install git`
* RVM
  * With Homebrew and Git in place, check out the download and installation instructions at https://rvm.beginrescueend.com/

<div class="note">
<p>If downloading XCode will take you too long, you can try using the unofficial GCC compilers available here: <a href="https://github.com/kennethreitz/osx-gcc-installer">https://github.com/kennethreitz/osx-gcc-installer</a></p>
</div>

### Linux

If Mac OS isn't a possibility, then your next best bet is Linux. Among distributions, Ubuntu has the best support for Ruby and Rails development. You'll need:

* Git (`sudo apt-get install git-core`)
* RVM (<http://ryanbigg.com/2010/12/ubuntu-ruby-rvm-rails-and-you/>)

You want to avoid managing Ruby, RubyGems, etc. through your package management solution (`apt`). The packages available usually lag months behind the real source code repositories, and it is going to cause you massive headaches.

Instead, setup RVM and handle everything through there (as we'll discuss in the next section).

If you're going to be doing Rails work, then you should also install Node.js. You can get it from your distribution's package manager. If you're using Ubuntu, like above:

`sudo apt-get install node`

### Windows

Getting started on the Windows platform is actually very easy. Engine Yard (<http://engineyard.com>) has put together the RailsInstaller (<http://railsinstaller.org/>), a single package installer with all the tools you need to get working. Make sure that, during the setup, you check the box to configure your environment variables.

Beyond initial setup, though, there is going to be pain. As you add in more Gems and other dependencies you'll find that many of them utilize _native extensions_, code written in C for better performance. Unless the authors have put energy into being cross-platform, you'll run into issues.

<div class="opinion">
<p>If there is any way to avoid using Windows for your development environment, do it. For a free alternative, consider setting up a virtual machine with <a href="http://www.virtualbox.org">Virtual Box</a> and <a href="http://www.ubuntu.com/download/ubuntu/download">Ubuntu Linux</a>.</p>
</div>
