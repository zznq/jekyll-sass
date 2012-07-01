Less for Jekyll
===============

This gem provides a [Jekyll](http://github.com/mojombo/jekyll) converter for
[Sass](http://http://sass-lang.com//) files.

Basic Setup
-----------
Install the gem:

	[sudo] gem install jekyll-sass

In a plugin file within your Jekyll project's _plugins directory:

	# _plugins/my-plugin.rb
	require "jekyll-sass"

Place .scss files anywhere in your Jekyll project's directory.  These will be
converted to .css files with the same directory path and filename. For example,
if you create a Less file at _css/my-stuff/styles.scss, then the corresponding
css file would end up at _css/my-stuff/styles.css_.

Bundler Setup
-------------
Already using bundler to manage gems for your Jekyll project?  Then just add

	gem "jekyll-sass"

to your gemfile and create the following plugin in your projects _plugins
directory.  I've called mine bundler.rb.  This will automatically require all
of the gems specified in your Gemfile.

	# _plugins/bundler.rb
	require "rubygems"
	require "bundler/setup"
	Bundler.require(:default)

Credit
------
This gem is based on [Roger López's](https://github.com/zroger) [jekyll-less](https://github.com/zroger/jekyll-less).
