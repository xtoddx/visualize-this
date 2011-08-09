_layout.yaml_ holds basic formatting information per chapter.

I've used hashes for everything, and numbered keys begin with 1.  This is to
keep with the patter of chapters, which also begin at one.

An example of traversing this data is provided below, in [ruby](http://ruby-lang.org).

	require 'yaml'
	chapters = YAML.load(File.read('layout.yaml'))
        puts "Chapter 1 is called #{chapters[1]['title']}"
        puts "Chapter 1 has #{chapters[1]['sidebars'].length} sidebars"
        puts "Chapter 1 has #{chapters[1]['sections'].length} primary sections"
