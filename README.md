pydailystrips
=============

A python replacement for the old comics page reader, dailystrips.

pydailystrips will create your own comics page for you. Just run it with the names of the comic strips you would like to include, and it will create an HTML page which you can use to read all your comics in one place. 

usage: pydailystrips [-h] [-o OUTPUT] [-i INPUT] [-v] [--defs DEFS]
                     [strips [strips ...]]

positional arguments:
  strips                strips to load, separated by spaces

optional arguments:
  -h, --help            	show this help message and exit
  -o OUTPUT, --output OUTPUT	output file to write to
  -i INPUT, --input INPUT	input file to read from
  -v, --version     	    	print version and exit
  --defs DEFS           	Path to the strip definition file


Sample usage:
  $python pydailystrips dilbert, garfield, dennis-the-menace
  $python pydailystrips -i list_of_strips
  $python pydailystrips -i list_of_strips -o mypage.html

Requirements:
* Runs in Python 2.7. I have gotten it to work in Python 2.6 also, but you have to install argparse manually as it isn't included in 2.6 by default.

Goals:
* Use the dailystrips comics definition format for interoperability
* Update everything
* Run in python
* Use github to keep the comic definitions up to date. (A major gripe of mine with the old dailystrips which hasn't been updated in years).

What's changed since dailystrips:
* prefetch has been removed, instead the referer header is now supported
* strips.def file has been updated. Dead strips removed, new ones added.
* The program is much simpler, easer to manage, and runs in python.
