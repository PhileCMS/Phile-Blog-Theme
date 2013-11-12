Phile-Blog-Theme
================

This is a theme developed to showcase how blogging works on [Phile](https://github.com/PhileCMS).

### Important!

Please use a fresh Phile installation in order to avoid errors not associated with this theme/demo.  These instructions assume you are doing so.

### Installation
First, [download a fresh copy of Phile](https://github.com/PhileCMS/Phile/archive/master.zip) and install in your chosen webserver directory

Next, [download a copy of Phile-Blog-Theme](https://github.com/james2doyle/Phile-Blog-Theme/archive/master.zip) and drop the folder into the root directory that Phile was installed into.

Now we have a little bit of unpacking / adjusting to do.  Open Phile-Blog-Theme-master.zip, and move copies of two folders:

1: Find Phile-Blog-Theme-master > themes > blog and move to your-install-of-Phile > themes (so now you  should have two folders in the 'themes' folder: default and blog)

2: Find Phile-Blog-Theme-master > content and use it to replace your-install-of-Phile > content

3: Replace the contents of your-install-of-Phile >config.php with the following:

 
	<?php
		
		// use this config file to overwrite the defaults from default_config.php
		// or to make local config changes.
		$config = array();
		
		// set the theme for this installation
		$config['theme'] = 'blog';
		
		// set some defaults for the pages
		$config['date_format'] = 'jS F, Y'; // 11th November, 2013
		$config['pages_order_by'] = 'date'; // this is a blog so date ordering
		$config['pages_order'] = 'desc';
		
		// disable the cache for this theme since we are in development
		$config['plugins'] = array(
		'philePhpFastCache' => array('active' => false),
		'phileSimpleFileDataPersistence' => array('active' => false)
		);
		
		// it is important to return the $config array!
		return $config; 

### Done!

That should be it.  When you have completed the above, point your browser to your newly installed Phile CMS, and you should see something like this screenshot:
<hr>
![Blog install screen shot](http://snippe.ca/sandbox/blog-screenie.jpg "Blog install screenshot")
<hr>

### Next?

This install has sample files for both pages and posts.  Take a look at the way they are set up... there is an important difference.  "Posts", which is what your blog entries are, have a Date:YYYY/MM/DD field up at the top.  "Pages" do not.  This is an important fact to keep in mind, as this is how Phile knows which is which, and is also how this blog theme sorts and shows the posts.  Further, the date meta makes sure that blog posts do not show up in your page navigation.

Here is the 'header' for a blog post (from the samples provided):

	/*
		Title: Fake Blog Post 1
		Description: This post is not real
		Date: 2013/11/08
		Category: PHP
		Keywords: PHP, CMS, Phile, Markdown, Twig
		Template: post
		*/
		
And here is one for a page (again, from the samples provided):

	/*
		Title: Another
		Description: This description will go in the meta description tag
		*/
		
There are other differences, which are noted within the sample files.  Please review those to help you get a better understandoing of how this works.  

Enjoy! These are still early days... stay tuned for new features!
