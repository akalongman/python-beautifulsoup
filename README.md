# BeautifulSoup (HTML/XML Formatter on python)

This is fork of BeautifulSoup by Leonard Richardson

Added some extra options, like indent_size



## Introduction

Beautiful Soup is a Python library designed for quick turnaround projects like screen-scraping. Three features make it powerful:

Beautiful Soup provides a few simple methods and Pythonic idioms for navigating, searching, and modifying a parse tree: a toolkit for dissecting a document and extracting what you need. It doesn't take much code to write an application

Beautiful Soup automatically converts incoming documents to Unicode and outgoing documents to UTF-8. You don't have to think about encodings, unless the document doesn't specify an encoding and Beautiful Soup can't detect one. Then you just have to specify the original encoding.

Beautiful Soup sits on top of popular Python parsers like lxml and html5lib, allowing you to try out different parsing strategies or trade speed for flexibility.

Beautiful Soup parses anything you give it, and does the tree traversal stuff for you. You can tell it "Find all the links", or "Find all the links of class externalLink", or "Find all the links whose urls match "foo.com", or "Find the table heading that's got bold text, then give me that text."

Valuable data that was once locked up in poorly-designed websites is now within your reach. Projects that would have taken hours take only minutes with Beautiful Soup.



```
  >>> from bs4 import BeautifulSoup
  >>> soup = BeautifulSoup("<p>Some<b>bad<i>HTML")
  >>> print soup.prettify()
  <html>
   <body>
    <p>
     Some
     <b>
      bad
      <i>
       HTML
      </i>
     </b>
    </p>
   </body>
  </html>
  >>> soup.find(text="bad")
  u'bad'

  >>> soup.i
  <i>HTML</i>

  >>> soup = BeautifulSoup("<tag1>Some<tag2/>bad<tag3>XML", "xml")
  >>> print soup.prettify()
  <?xml version="1.0" encoding="utf-8">
  <tag1>
   Some
   <tag2 />
   bad
   <tag3>
    XML
   </tag3>
  </tag1>
```

## Full documentation

The bs4/doc/ directory contains full documentation in Sphinx
format. Run "make html" in that directory to create HTML
documentation.

## Running the unit tests

Beautiful Soup supports unit test discovery from the project root directory:

 $ nosetests

 $ python -m unittest discover -s bs4 # Python 2.7 and up

If you checked out the source tree, you should see a script in the
home directory called test-all-versions. This script will run the unit
tests under Python 2.7, then create a temporary Python 3 conversion of
the source and run the unit tests again under Python 3.

## Links
Origina l version: https://www.crummy.com/software/BeautifulSoup/
