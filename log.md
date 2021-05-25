# Part 2 Log

Edward Adam Payzant
SN: 101082175

Following the "Going Further Sequence"

## R

While I have a fair amount of programming experience, this is actually my first time using R. 
Just looking at the syntax, it's a rather foreign looking language to me with things like the variable assignment operator appearing to be `<-` instead of the usual `=`.

When displaying the cities and article count, there is a single mispelling of Edinburgh in the data. 
This should be a relatively simple fix, assuming tables are like dictionaries/objects/maps where I can just add the value at "Edinbugh" to "Edinburgh" then remove the "Edinbugh" column.
Adding the value is relatively easy and can be done with `counts["Edinburgh"] <- counts["Edinburgh"] + counts["Edinbugh"]`.
Removing the typo column is seemingly a little trickier however.
A lot of the public documentation appears to focus on dealing with dataframes, not tables, which means I went down a few paths that were completely wrong.
This should be a relatively quick fix, but annoyingly I ran out of time to complete it.

To do some additional graphs, I decided to look at the per-month article distribution. 
This allowed me to make the interesting observation that the most amount of articles are published in September, followed by January, then December.

**TODO: Do some more visualizations**

## Wget

After doing the R tutorial, it's nice to get back to something I relatively know. I've not really used many of the features beyond basically using as curl but it'll follow links however, so there is some new content. 
Going through the tutorial, I had no issues. 
I've used both wget and python on this machine before, so everything was already known to be working, and it was otherwise just following through the tutorial.

Also, on a somewhat terrifying side note, there are at least several people (notably Richard Stallman) that exlcusively use wget to browse the web due to the free software disputes with JS. I can't imagine it's a nice way to go through the modern web, but it's impressive you can still achieve that with just wget.

## An intro to APIs

Oh boy, APIs.
I have some experience with them, mainly with some simple website projects and a discord bot, but they were all relatively straightforward and I know that's not always the norm.
The GLAM Workbench looks interesting, but I ran out of time with this part to take a look. 
Hopefully I can do a proper dive at a later point because it certainly looks interesting.

## REGEX

I do have some regex experience, but that was mainly from using the `grep` command
I have frequently referred to regex as "black magic".
Mostly I resolve any regex questions with a Google search and some basic knowhow, but it's still fairly poor.

I'll be writing this as I go, with some editing after I'm finished. 
Looking at step 4, I misread it and thought I was just to strip all of the html and spent far too long finding it.
After some hunting for the proper way to remove all the html, I settled on using `<PRE>(.|\n)*?<\/PRE>` to select the pre tags and all the content between them.
Then I just cut the selected, cleared the file, the pasted the content back in.
It's not the most elegant, but it worked.
Also, to remove the pre tags, matching `</?pre>`.
After going through all the effort of figuring this out, I then read the next line of that instruction and was immediately annoyed at myself.
After figuring out how to remove the html however, actually scraping the tables is very easy and I can just match using `Sam Houston to J. Pinckney Henderson, December 31, 1836 51(.|\n)*?Wm. Henry Daingerfield to Ebenezer Allen, February 2, 1846 1582`.
I once again couldn't get select inverse to work, so I had to repeat the cut, clear file, paste.
Coming into step 5 is where I learned VSCode and Sublime appear to have slightly different regex engines.
I tried to get it working, but caved and just installed sublime.
After switching to sublime, everything was pretty straightforward.

## An Intro to Python and Jupyter

I'm quite confident with Python and to a lesser extent Jupyter Notebooks, but I still went through it just as a refesher.
It was a solid refresher, and notably reminded the fun local vs global scoping problem (in python-basics-2) where global variables in functions need to be specified as global.