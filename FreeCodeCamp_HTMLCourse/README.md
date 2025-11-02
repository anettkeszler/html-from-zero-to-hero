# FreeCodeCamp HTML Course on YouTube 

Course link : https://www.youtube.com/watch?v=kUMe1FH4CHE&t=11s

## Chapter1: Getting Started

### What is HTML? 
HTML **(HyperText Markup Language)** is the most basic building block of the Web. It defines the meaning and structure of web content. 

"Hypertext" refers to links that connect web pages to one another.

HTML uses "markup" to annotate text, images and other content for display in a Web browser. HTML markup includes special elements such as head, title, body, header, footer, article ... 

### Index.html file

Create **index.html** file - this is always the file name that is expected to launch a website.


```<html></html>``` element (opening and closing tags) - every page starts and ends with this tag and everything else on the page goes between those tags 

```<head></head>``` element - all metadata comes here which is not visible on the page 

```<body></body>``` element - contains all visible data 

```<title></title>``` elment in the ```<head>``` tags gives a title to your website, it will be visible in the tab when you open your website in the browser 

```<h1></h1>``` element - Biggest heading (h1-h6)

```<p></p>``` element - paragraph 

### Useful Extensions

1. To intend nicely your html code, use **Prettier - Code formatter** extension to autoformat your code 


2. Download **Live Server** from Extension - it is going to help us to view our web page. 

### Go Live

Right click on the file name and 'Open with Live Server' 

http://127.0.0.1:5500/FreeCodeCamp_HTMLCourse/Chapter1_GettingStarted/index.html - this is the address of the webpage, it contains the IP address (127.0.0.) + port number (5500). This runs only on my computer at the moment, we haven't loaded it to the web. This created only a local server, it's called a dev environment. 

To stop the server, click on the button 'Port: 5500' in the right botton corner OR right click on the file 'Stop Live Server'. 

### Validation

To validate your HTML code, use validator: https://validator.w3.org/

Upload the index.html file for validation. You get some errors. 
"Warning: consider to add a lang attribute to the html start tag to declare the language of this document". - Let's fix this by adding 'lang' attribute. ```<html lang="en">```

"Error: The character encoding was not declared" - 
```<meta charset="UTF-8">``` write this into the head tag 

"Error: Start tag seen without seeing a doctype first. Expected ```<!DOCTYPE html>```" - Documentum type declaration should stand in the very first line of every html file. 


## Chapter2: Head Element

Everything inside in the ```<head>``` element is not seen on the webpage, it contains meta data

```
<meta name="author" content="Anett Keszler">
<meta name="description" content="This page contains all the things I am learning how to create as I learn HTML">
```

The ```<meta>``` element attributes (name, content) can be picked up in search engines or some other service that wants to learn more about our web page.

```<link>``` element: 
```        
<link rel="icon" href="html.png" type="image/x-icon">
```
It will add the small icon beside the title in the tab when opening in browser.

Add css file and reference to it in the html file:

```
<link rel="stylesheet" href="main.css" type="text/css">
```

## Chapter3: Text Basics

- Headings
: ```<h1>``` to ```<h6>```

    It gives a semantic meaning to the text, there is a hyerarchy between them.

- Paragraph: ```<p></p>```  
- Address: ```<address></address>``` to provide address nicely

- Horizontal line: ```<hr>``` 

- Line break: ```<br>```  - html doesn't care about whitespaces, it will ignore them. So use line break to add extra empty lines. 

- Emphasize: ```<em></em>``` inline element, it emphasizes/italisizes the text.

- Strong / bold: ```<strong></strong>``` inline element, it makes bigger and bolder the text.

- Abbreviation: ```<abbr></abbr>```, add an attribute to abbr to get a meaning --> title. 
```<abbr title="Mozilla Developer Network">MDN</abbr>```

- comment in html file - it is not visible on the web page but visible in the source code.i
```<!-- TODO: Add more places-->```

**Inline elements**: em, strong, abbr

**Block level elements**: h1 - h6, p

- HTML entities

```&nbsp;``` it creates a ' ' (space). 

```&lt;``` and ```&gt;``` and ```&copy;``` - less than, greather than and @ sign. 

```
        &lt;&lt;&lt; &copy; Anett Keszler &gt;&gt;&gt;
        <<< © Anett Keszler >>>
```








