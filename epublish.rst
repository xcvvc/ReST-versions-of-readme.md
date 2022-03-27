epublish example
================

========================
two helpful Kindle files
========================

When publishing for Kindle, there are two essential files.  The table of contents file has a few special Amazon tags.   The navigation file connects the table of contents to the Kindle's drop down navigation bar.  

navigation.nav

toc.html

there are three books.  Note that the .nav file differs only in author and title.

========================
a navigation file sample
========================
::

    <?xml version="1.0"?>
    <!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN" "http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">
    <ncx xmlns-"http://www.daisy.org/z3986/2005/ncx/" version="2005-1">
    <head>
    <meta name="dtb:uid" content="bookid"/>
    <meta name="dtb:depth" content="1"/>
    <meta name="dtb:totalPageCount" content="0"/>
    <meta name="dtb:maxPageNumber" content="0"/>
    </head>

    <docTitle><text>Ballet with Mother:&nbsp;&nbsp; Technical Stage and Production script</text></docTitle>
    <docAuthor><text>Kop'ye Zoloto</text></docAuthor>
    
    <nav epub:type="landmarks" class="hidden-tag" hidden="hidden">
    
    <ol class="none" pub:type="list">
    <li><a epub:type="toc" href="toc.html">Table of Contents</a></li>
    </ol>
    </nav>
    </ncx>

==========================
a table of contents sample
==========================

::

    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
    <meta http-equiv="content-type" content="text/html; charset=UTF-8" />
    </head>
    
    <body>
    <center>Table of Contents</center>
    <p />
    <nav epub:type="toc">
    <ol>
    <li><a href="stagetech.html#titlepage">
    
    English Title Page
    </a></li><li><a href="stagetech.html#castsheet">
    Cast
    </a></li><li><a href="stagetech.html#scene_list">
    Scenes 
    </a></li><li><a href="stagetech.html#going_out">	
    
    Scene one</a>: Getting to the Opera House and being seated in the balcony.
    </li><li><a href="stagetech.html#pianist">
    
    Scene two</a>: Frustrated Pianist meets Odile
    </li><li><a href="stagetech.html#shop">
    Interlude scene two</a>: Mother and Daughter visit the gift shop.
    </li><li><a href="stagetech.html#palace">
    
    Scene three</a>: Siegfried's palace celebrations with Odette.
    </li><li><a href="stagetech.html#attention">	
    Interlude Scene three</a>: Mother holds Daughter's attention between scenes.
    </li><li><a href="stagetech.html#home">
    
    Scene four</a>: Odile's bed chamber
    </li><li><a href="stagetech.html#closer">
    Interlude Scene four</a>: Closer seating with the Usher
    </li><li><a href="stagetech.html#battleground">
    
    Scene five</a>: Siegfried's losing battle
    </li><li><a href="stagetech.html#cleanup">
    (optional) Interlude Scene five</a>: Audience watches a set change 
    </li><li><a href="stagetech.html#gifts">
    
    Scene six</a>: Pianist is grateful to Odile
    </li>
    <li><a href="stagetech.html#german">
    <i>Deutsche</i>
    </a></li>
    <li><a href="stagetech.html#italian">
    <i>Italiana</i>
    </a></li>
    <li><a href="stagetech.html#french">
    <i>Française</i>
    </a></li>
    <li><a href="stagetech.html#taiwan">
    中文&nbsp;&nbsp;&nbsp;(Ch)
    </a></li>
    <li><a href="stagetech.html#japan">
    日本語&nbsp;&nbsp;&nbsp;(Jp)
    </a></li>
    </ol>
    
    </nav>
    </body>
    </html>


