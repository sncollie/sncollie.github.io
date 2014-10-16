---
layout: post
title:  "Windows Users Unite!  (after the service pack gets released)"
date:   2014-10-16 12:02:11
categories: jekyll update
---
#Jekyll in Windows
I can admit it...I'm a Windows user.  Normally, this isn't a big deal (I'll avoid getting into those Mac/MS/Linux fanboy arguments).

<img src="/images/darthms.jpg" class="blog-images">

<span class="blog-text"><i>I hear they have cookies</i></span>

But I'm learning to be a devleoper.  Using Windows is like trying to use a shoe to hammer in a nail.  It's doable, but it takes longer...and usually ruins the shoe...and the wall...and probably the nail, too.

So I've found a few links to get the wary Windows user up and running using Jekyll.

The best site I've found so far:  

<a href="http://jekyll-windows.juthilo.com/">Run Jekyll on Windows</a>

It's pretty straightforward, and MOST people will get it working.

I was not one of those people.  If you're like me (may God have mercy on your soul), here's the trick.

There is one last teeny-tiny step you need to do.

Add the following to your `dk.rb' file.  this file is located in the Ruby Development folder (where ever you chose to put it).  Find the existing REG_KEYS entry and replace with this:


    REG_KEYS = [
	    'Software\RubyInstaller\MRI',
	    'Software\RubyInstaller\Rubinius',
	    'Software\Wow6432Node\RubyInstaller\MRI'
		]


Without it, I could not get jekyll server to run.



[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
