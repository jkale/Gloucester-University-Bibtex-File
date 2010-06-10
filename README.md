About
=====

This repo contains a .bst file which, when used with LaTeX and BiBtEx, will output references in the University of Gloucestershire's Post Graduate format (for the school of Business). This format is loosely based on APA but as far as I can see it's fairly different. 

Maturity
========

I'm using this for my own MSc Diss and have only so far tested it as working using this. There may still be inconsistencies with the Uni's guide; YMMV.

Usage
=====

Tested most throughly with the natbib package (I don't really use any of the apa* variants anymore). Place this code in your preamble.

`\usepackage[longnamesfirst]{natbib}`

The "longnamesfirst" option complies with the University's stance on how in text citations should be performed (all the authors named in the first citation, first three with et al appended thereafter).

If you wish to cite a website your BiBtEx record **must** have the correct fields. These are `url` and `accessed-date`. An example is the following:

`
@misc{eure:2009,
	Accessed-Date = {September 9th, 2009},
	Author = {Ian Eure},
	Date-Added = {2010-06-07 19:57:59 +0100},
	Date-Modified = {2010-06-07 20:00:43 +0100},
	Keywords = {nosql; MSc Diss; Cassandra; cap},
	Month = {September},
	Title = {Looking to the Future with Cassandra},
	Url = {http://about.digg.com/blog/looking-future-cassandra},
	Year = {2009}
}
`

To obtain the correct formatting, write accessed-date in the format above (month day, year). This bst performs no custom formatting on it (though I may add this at a later date).