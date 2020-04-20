---
layout: lesson
---
Installing Ruby, bundler, and Jekyll on  a Windows10 computer
======================

Installing Software
If you want to set up Jekyll so that you can preview changes on your own machine before pushing them to GitHub, you must install the software described below. (Note: Julian Thilo has written instructions for installing Jekyll on Windows.)
1.	Ruby. This is included with Linux and macOS; the simplest option on Windows is to use RubyInstaller. You can test your installation by running ruby --version. For more information, see the Ruby installation guidelines.
2.	RubyGems (the package manager for Ruby). You can test your installation by running gem --version.
3.	Jekyll. You can install this by running gem install jekyll.
Setting Up a Separate Repository for Learners
If you are teaching Git, you should create a separate repository for learners to use in that lesson. You should not have them use the workshop website repository because:
•	your workshop website repository contains many files that most learners don't need to see during the lesson, and
•	you probably don't want to accidentally merge a damaging pull request from a novice Git user into your workshop's website while you are using it to teach.
You can call this repository whatever you like, and add whatever content you need to it.
Getting and Giving Help
We are committed to offering a pleasant setup experience for our learners and organizers. If you find bugs in our instructions, or would like to suggest improvements, please file an issue or mail us.
INSTALL Ruby for Windows:
1.	Download and Install Git for Windows which installs the GitBash Terminal: https://gitforwindows.org/
a.	After installing Git (if already installed, make sure it is upgraded to latest version) use Git to connected to github to download spreadsheet-ecology-lesson from Data Carpentry site.
b.	Update to latest version using `git update`, then close Git Window.
2.	Ruby: On Windows 10: 
a.	Downloaded the Ruby for Windows installer rubyinstaller-devkit-2.6.6-1-x64.exe from  https://rubyinstaller.org/
b.	Run the RubyInstaller (Run as Administrator) 
c.	After installer completes (see last image shown below), hitting “enter” exits the `cmd.exe` prompt
d.	Re-open `cmd.exe`: You can test your installation by running `ruby –version`
i.	C:\WINDOWS\system32>gem --version
3.0.3
ii.	C:\WINDOWS\system32> ruby --version
ruby 2.6.6p146 (2020-03-31 revision 67876) [x64-mingw32]

e.	Ruby install is now in the Windows10 Environment Variables and the PATH
f.	RubyGems (the package manager for Ruby) v3.0.3 should already installed in your Ruby environment
g.	NOTE: on this site: https://www.rubydoc.info/github/rubygems/rubygems
i.	Check by running `gem –version` in your cmd.exe terminal window.
ii.	Installing Ruby via Windows `cmd.exe` extended Ruby functions to GitBash!!!!
iii.	Check that Ruby is available from GitBash:
1.	$ ruby --version
2.	ruby 2.6.6p146 (2020-03-31 revision 67876) [x64-mingw32]
iv.	Check that gems are working from GitBash
1.	Pete@Bluegenes64 MINGW64 ~
2.	$ gem --version
3.	3.0.3
h.	Reopen & Run as Administrator; the Windows `cmd.exe` (NOT Ruby command window which will show up in your start menu)
i.	C:\WINDOWS\system32>gem --version
3.0.3
i.	Update your RubyGems from inside the Windows `cmd.exe` Run as Administrator. This will also install `bundler`!!
i.	C:\WINDOWS\system32>gem update --system
```
Updating rubygems-update
Fetching rubygems-update-3.1.2.gem
Successfully installed rubygems-update-3.1.2
Parsing documentation for rubygems-update-3.1.2
Installing ri documentation for rubygems-update-3.1.2
Installing darkfish documentation for rubygems-update-3.1.2
Done installing documentation for rubygems-update after 248 seconds
Parsing documentation for rubygems-update-3.1.2
Done installing documentation for rubygems-update after 0 seconds
Installing RubyGems 3.1.2
  Successfully built RubyGem
  Name: bundler
  Version: 2.1.2
  File: bundler-2.1.2.gem
Bundler 2.1.2 installed
RubyGems 3.1.2 installed
Regenerating binstubs
Parsing documentation for rubygems-3.1.2
Installing ri documentation for rubygems-3.1.2

(LOTS of info about updates)

RubyGems installed the following executables:
        C:/Ruby26-x64/bin/gem
        C:/Ruby26-x64/bin/bundle

Ruby Interactive (ri) documentation was installed. ri is kind of like man
pages for Ruby libraries. You may access it like this:
  ri Classname
  ri Classname.class_method
  ri Classname#instance_method
If you do not wish to install this documentation in the future, use the
--no-document flag, or set it as the default in your ~/.gemrc file. See
'gem help env' for details.

RubyGems system software updated

C:\WINDOWS\system32>
```
3.	Now Install Jekyll under the Winodows cmd.exe terminal window (no need to exit your currently running terminal) 
`gem install Jekyll.`
```
a.	(Lots of fetching then installing…)
b.	(Warnings about breaking Rails fallbacks)
c.	Example: 
Jekyll 4.0 comes with some major changes, notably:

  * Our `link` tag now comes with the `relative_url` filter incorporated into it.
    You should no longer prepend `{{ site.baseurl }}` to `{% link foo.md %}`
    For further details: https://github.com/jekyll/jekyll/pull/6727

  * Our `post_url` tag now comes with the `relative_url` filter incorporated into it.
    You shouldn't prepend `{{ site.baseurl }}` to `{% post_url 2019-03-27-hello %}`
    For further details: https://github.com/jekyll/jekyll/pull/7589

  * Support for deprecated configuration options has been removed. We will no longer
    output a warning and gracefully assign their values to the newer counterparts
    internally.
Done installing documentation for public_suffix, addressable, colorator, http_parser.rb, eventmachine, em-websocket, concurrent-ruby, i18n, ffi, sassc, jekyll-sass-converter, rb-fsevent, rb-inotify, listen, jekyll-watch, kramdown, kramdown-parser-gfm, liquid, mercenary, forwardable-extended, pathutil, rouge, safe_yaml, unicode-display_width, terminal-table, jekyll after 182 seconds
26 gems installed
C:\WINDOWS\system32> 
```
4.	Close Windows command terminal: 
5.	Open Gitbash Window
a.	Check RubyGems install, and Jekyll install:
Pete@Bluegenes64 MINGW64 ~
$ gem --version
3.1.2

Pete@Bluegenes64 MINGW64 ~
$ jekyll --version
jekyll 4.0.0

Pete@Bluegenes64 MINGW64 ~
$ pwd
/c/Users/Pete

6.	Change directories into your local Git repository, e.g. “Spreadsheet-ecology-lesson (gh-pages)”
a.	Run Jekyll serve: 
```
Pete@Bluegenes64 MINGW64 ~/git/spreadsheet-ecology-lesson (gh-pages)
$ jekyll serve
Configuration file: C:/Users/Pete/git/spreadsheet-ecology-lesson/_config.yml
            Source: C:/Users/Pete/git/spreadsheet-ecology-lesson
       Destination: C:/Users/Pete/git/spreadsheet-ecology-lesson/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 9.541 seconds.
  Please add the following to your Gemfile to avoid polling for changes:
    gem 'wdm', '>= 0.1.0' if Gem.win_platform?
 Auto-regeneration: enabled for 'C:/Users/Pete/git/spreadsheet-ecology-lesson'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```


NOTE: a  “.jekyll-cache” folder may appear which MUST be IGNORED

1.	Add this folder to .gitignore 
2.	Add this folder to “exclude” in the _config.yml file
This works but I’ll need to formally add this to the lesson as a PR. Use a message such as “fix for Jekyll-cache”. AND use a different branch
Use branch hoyt2: Submitted PR and François said he’s look at it. (on Mar-47,2020)
