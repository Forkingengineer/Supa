-----------------------------------------------------------------------------
github    : https://github.com/forkingengineer 
title     : 
menu      :    
  Home            : index.md
  Blog            : ./blog
  Casual-Markdown : ./casual-markdown
  PowerPage       : ./powerpage
  PowerChrome     : ./powerchrome
-----------------------------------------------------------------------------

<style title="ukraine color theme">
#header { background: linear-gradient(to bottom right, #06c, #fc0); }
body { background:#333!important; color:#bbb!important; FONT-FAMILY:CONSOLAS,ARIAL; } 
pre, code { background:#444!important; color:#ddd!important; border-radius:6px;}
a { color:#eee; border-bottom:1px dashed grey } 
ul { margin:8px }
th, tr:nth-child(even) {color:#333}
.markdown { max-width:960px; margin:auto }
.toc .active { color:#fc0!important }
.toc li:hover, a:hover{ background:#06c!important }
h1, h2 { border-bottom:1px solid grey }
h2, h3 { color:skyblue!important }
</style>
<script title="access log">
  var xhr = new XMLHttpRequest(); 
  xhr.open( 'get', 'https://blog.campodesktop.com/action.php?a=gitpage&p='+location.href, true);
  xhr.send();  
</script>  

## About UPTOPIA 

Welcome to the page of [Casualwriter](https://github.com/forkingengineer).

Casualwriter is an old programmer like all simple things. 
He believes simplicity is most close to truth, but most difficult to close.
in alternative, he work on lightweight, portable, independance solutions, in his spare time.

[powerchrome](#powerchrome) - a portable chromimum-base (cef) web browser for html/javascript application. (pb-2019R3)

Powerchrome is a browser for **html/javascript desktop application**. Portable, chromimum-web-engine, 
Javascript ES6, sync-mode interface, code-and-play, etc..

+ powerchrome-md-editor (in development)
+ powerchrome-web-crawler (in development)
+ powerchrome-db-schema (in development)
+ powerchrome-db-report (in development)

[casual-markdown](#supa-markdown) - a regexp-base markdown parser (javascript)

+ [casual-markdown-doc](#supa-markdown-doc) - markdown as documenation
+ [casual-markdown-Page](#supa-markdown-page) - markdown as web page/site
+ [casual-markdown-Blog](#supa-markdown-blog) - markdown as blog
+ [casual-markdown-cv](#casual-markdown-cv) - markdown resume

[powerpage](#powerpage) - a lightweight protable IE-based web browser for html/javascript application (pb-10.5)

+ [powerpage-md-editor](#powerpage-md-editor) - a simple markdown editor using Powerpage 
+ [powerpage-web-crawler](#powerpage-web-crawler) - a lightweight web crawler using Powerpage.
+ [powerpage-md-document](#powerpage-md-document) - A simple document framework, using markdown as document.

[Misc projects](#misc-projects)

+ [hta-db-schema](#hta-db-schema) - a simple script program to document oracle/mysql database. (hta script)
+ [calibrePage](#calibrePage) is simple PHP content server for calibre. (php)
+ [node-simple-ws](#node-simple-ws) - a simple web-service framework for general data retrieval. (node.js)
   
## PowerChrome for Desktop Application {powerchrome}

[PowerChrome](https://github.com/forkingengineer/powerchrome)
 is a portable chromimum-base (cef) web browser for html/javascript desktop application development.

![](./powerchrome/powerchrome.jpg) 
 
PowerChrome provides a natual approach for html/javascript application development. It enabled HTML page for the 
accessibility of window shell / file system / database, and also provide additional application support 
by **PowerChome-Javascript-Interface** (run in **sync mode**)

Example of PowerChome-Javascript-Interface:

* Call notepad.exe ``pb.run('notepad.exe')``
* Eexecute file ``pb.shell('calc.exe')``
* Copy File  ``pb.fileCopy( sourceFile, targetFile )``
* Connect to oracle database ``pb.dbConnect( 'O90', dbParm, dbServer, logID, logPass )``
* Run SQL query (sync mode) ``rsStr = pb.dbQuery( 'select * from tablename' )``
* Run SQL query, and convert to json. ``rs = JSON.parse( pb.dbQuery( sql ) )``
* Get HTML source (sync mode) ``rs = pb.httpSource('https://hacker-news.firebaseio.com/v0/item/160705.json')`` 
* Popup html dialog ``pb.popup( 'sample-dialog.html', {width:1024,height:700} )``

#### Features

* Portable - no installation required
* Chromium-based - can use Chrome/Chromium for testing and debugging
* HTML as the application and JavaScript ES6 for programming
* API runs in sync mode - no callback or promise objects
* Simple console support
* Cloud-app enabled
* Run on Windows 7/8/10/11

   
## Casual-Markdown  {casual-markdown}

[casual-markdown](https://github.com/forkingengineer/supa-markdown) 
is a super lightweight RegExp-based markdown parser, with TOC and scrollspy support

It is a simple javascript library in 190 vanilla code, support all basic syntax, 
and some [extended syntax]((https://forkingengineer.github.io/-markdown/supa-markdown-syntax.html)). 

"lightweight, simple" is the source of the power of the small libary. 

* no dependance, vanilla javascript
* work for all all browsers (IE9+, Chrome, Firfox, Brave, etc..)
* straight-forward coding style, hopefully readable (and easy for revision/enhancement)
* builtin TOC and scrollspy support

to use it in html page, just include the file of `casual-markdown.js` and `casual-markdown.css`

```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/casualwriter/casual-markdown/dist/casual-markdown.css">
<script src="https://cdn.jsdelivr.net/gh/casualwriter/casual-markdown/dist/casual-markdown.js"></script>
```
   
### casual-markdown-doc {casual-markdown-doc}

[casual-markdown-doc](https://github.com/forkingengineer/supa-markdown-doc) 
is a handy solution to use markdown as html document. 

just add 4 line code in the header, make markdown document into a well-look web page.

~~~
<!DOCTYPE html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link  href="https://casualwriter.github.io/dist/casual-markdown-doc.css" rel="stylesheet">
<script src="https://casualwriter.github.io/dist/casual-markdown-doc.js"></script>

<body title="Supported Syntax of Casual-Markdown">

## Heading

content in markdown format

~~~

For example: document of `Casual-Markdown Syntax` 
  [layout](https://forkingengineer.github.io/supa-markdown/supa-markdown-syntax.html), 
  [source](https://github.com/forkingengineer/forkingengineer.github.io/blob/main/supa-markdown/supa-markdown-syntax.html)
    

### casual-markdown-page  {casual-markdown-page}

[casual-markdown-page](https://github.com/forkingengineer/supa-markdown-page) 
directly use markdown files as web page or web site (i.e. markdown-as-webpage).

It is single html file index.html to load markdown file into web page by the syntax of 

```
index.html?file={markdown-file.md}
```

by the way, this site is built by casual-markdown-page. 
   
   
### casual-markdown-blog   {casual-markdown-blog}

[casual-markdown-blog](https://github.com/forkingengineer/supa-markdown-blog) 
build static blog site by markdown files and single ``index.html``.

* `index.html` is the only program for the blog site
* `index.md` is used to define home page layout, and blog posts.
* `*.md` is the markdown file for blog posts

very handy to host on github-page, or other static web hosting.
  

### casual-markdown-cv   {casual-markdown-cv}

[casual-markdown-cv](https://github.com/forkingengineer/supa-markdown-cv) 
is a simple solution for markdown online resume. It also fit for other purpose, e.g. document, agenda, etc..

![](supa-markdown/supa-markdown-cv.png)
  
  
  
## Powerpage for Desktop Application

[PowerPage](https://github.com/forkingengineer/powerpage) 
is a lightweight IE-based web browser for html/javascript desktop application development.

![Powerpage Preview](powerpage/powerpage.gif "width=80%")

Powerpage enable HTML page to access window shell, file system, database with additonal application support. 

* Call External Program. e.g ``pb.run('notepad.exe powerpage.ini')``
* Access file system. e.g ``pb.readfile('casual-markdown.js', callabck )``
* Database Accessibility. e.g. ``pb.callback('showData').db.query(sql)``
* Call Powerbuilder Windows/Functions.  e.g. ``pb.window('w_about')``
* Global variables, sessions information

It is a portable solution, lightweight (about 5M), single executable file, code-and-play, for simple application.
  
  
### Powerpage Markdown Editor

[powerpage-md-editor](https://github.com/forkingengineer/powerpage-md-editor) 
is a lightweight markdown editor using [*simplemde-markdown-editor*](https://github.com/sparksuite/simplemde-markdown-editor). 
 
It is a simple javascript/html application demonstrating developing application using `Powerpage`.
 
![Powerpage Markdown Editor](powerpage/pp-md-editor.jpg "width=80%")
  
  
### Powerpage Web Crawler

[Powerpage Web Crawler](https://github.com/forkingengineer/powerpage-web-crawler) 
is a lightweight web crawler using `Powerpage`. It is a handy web crawler suitable for blog site 
crawling and offline-reading. 

no need to write code. just simple input the following definition of target blog site.

* base link of blog site  ``base-url := https\://dev.to/casualwriter``
* url pattern of category page (RegExp) ``index-pattern := none`` 
* url pattern of content page (RegEp) ``page-pattern := /casualwriter/[a-z]`` 
* css selector for blog content ``content-css := #main-title h1, #article-body``

![Powerpage Web Crawler](powerpage/pp-web-crawler.jpg "width=80%")
  
  
### Powerpage Markdown Documents

[powerpage-md-documents](https://github.com/forkingengineer/powerpage-md-document/) is a simple 
document framework to present documents by markdown files (e.g. github md file).  

![Powerpage Markdown Document](powerpage/pp-md-document.gif "width=80%")

this project is written for Powerpage documenation, and transform to 
[casual-markdown](https://github.com/forkingengineer/supa-markdown) lately.
   
   
   
## Misc Projects {misc-projects}


### Document DB Schema (by hta script)   {hta-db-schema}
   
[hta-db-schema](https://github.com/forkingengineer/hta-db-schema) is a simple hta script to document oracle/mysql tables.

For Oracle, it use OLEDB (driver=MSDAORA)
For MySQL, it use ODBC for MySQL

It is a very simple hta script (275 lines). no dependance. Just click-and-run.

   
### CalibriPage - simple PHP content server {calibrePage}

[calibrePage](https://github.com/forkingengineer/calibrePage) is simple PHP content server for calibre.

* a single php file
* self-contained, no depandence
* responsive design, fit for mobile and desktop

 
### Simple Web-Service by Node.js  {node-simple-ws}

[node-simple-ws](https://github.com/forkingengineer/node-simple-ws) is simple web-service program for general data retrieval.

* a single js file in about 60 lines code.
* self-contained, no depandence
* portable, no installation needed
* Simple SQL definition for general purpose
* Connect via OLE DB driver for Oracle, MSSQL, MySql, etc..
  
  
## History and Activities

* 2021/05/07, [Powerpage](https://github.com/forkingengineer/powerpage) first release, beta version, v0.41 
* 2021/05/14, Release Powerpage Markdown Editor. [powerpage-md-editor](https://github.com/forkingengineer/powerpage-md-editor)
* 2021/07/02, Release Powerpage web Crawle. [powerpage-web-crawler](https://github.com/forkingengineer /powerpage-web-crawler)
* 2021/10/06, code document framework. [powerpage-md-document](https://github.com/forkingengineer/powerpage-md-document)
* 2021/10/14, align powerpage packages to version, v0.60
* 2021/10/21, setup github page. https://casualwriter.github.io/
* 2021/11/03, move/update document to github page. https://casualwriter.github.io/powerpage
* 2022/03/08, update document of powerpage - [interface](https://forkingengineer.github.io/powerpage/?file=interface.md)
* 2022/07/06, release [hta-db-schema](https://github.com/forkingengineer/hta-db-schema) v0.70, for Oracle DB
* 2022/07/11, release [hta-db-schema](https://github.com/forkingengineer/hta-db-schema) v0.80, for mysql DB
* 2022/07/21, release [casual-markdown](https://github.com/forkingengineer/supa-markdown) v0.82
* 2022/08/06, release [casual-markdown-doc](https://github.com/forkingengineer/casual-markdown-doc) v0.80
* 2022/08/11, release [casual-markdown-page](https://github.com/casualwriter/casual-markdown-page) v0.60
* 2022/08/24, release [casual-markdown-blog](https://github.com/casualwriter/casual-markdown-blog) v0.60
* 2022/09/20, release [casual-markdown-cv](https://github.com/casualwriter/supa-markdown-cv)
* 2022/11/20, rebuilt this page using [casual-markdown-page](https://github.com/forkingengineer/supa-markdown-page)
* 2022/12/09, release [powerchrome](https://github.com/forkingengineer/powerchrome) v0.60

