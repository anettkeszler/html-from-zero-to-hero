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

1. VSC: To intend nicely your html code, use **Prettier - Code formatter** extension to autoformat your code 

2. VSC: Download **Live Server** from Extension - it is going to help us to view our web page. 

3. Chrome: HTML5 Outliner Chrome Extension 

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

## Chapter4: List Types

- **Ordered list(ol)**: it is a numbered list, indented
```
<ol>
    <li>item1</li>
    <li>item2</li>
    <li>item3</li>
</ol>
```

- **Unordered list (ul)**: it creates a list with bullet point, indented
```
<ul>
    <li>item</li>
    <li>item</li>
    <li>item</li>
</ul>
```
- **Describtion list(dl)**: it has two different types of element: description term - **dt** and description details - **dd**.
```
<dl>
    <dt>North Pole</dt>
    <dd>I heard this is <strong>cold</strong>!</dd>
    <dt>South Pole</dt>
    <dd>This is also cold.</dd>
</dl>
```
Here the description terms are to the left, and the description details are indented 

## Chapter5: Add Links
- 'ht' in html is hypertext, and it is what links together everything on web
- 'anchor tag': creates a link to another page on the web 
```
<a href=""></a>

    <li>...I use resources from <abbr title="Mozilla Developer Network">
        <a href="https://developer.mozilla.org/en-US/">MDN</a>
    </abbr></li>
```

- href="https://developer.mozilla.org/en-US/" - this is an **absolute reference** to the website
- href ="html.png" - this is a **relative reference**, when the source is on our server, in this case in the same folder.
```
<a href="about.html">Anett Keszler</a>  // relative reference 
```
- **internal reference**: it is a link directly on the page

- **section** element: a semantic html element, represents a generic standalone section of a document.(**id attribute**)
```
    <section id="html"></section>
    <section id="vacation"></section>
```

- **nav** element: another semantic html element, represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.

```
<nav>
    <ul>
        <li><a href="#html">Learning HTML</a></li>
        <li><a href="#vacation">Planning a Vacation</a></li>
    </ul>
</nav>
```

- **Download a link**: with the **'download' attribute** in 'a' element clicking on the text it downloads the linked element.
```
Download an <a href="../Chapter2_HeadElement/html.png" download>HTML5 favicon</a>
```

- **Email address as a link**: 'mailto'
```
Contact me at <a href="mailto:random@gmail.com">my email address</a>
```
- **Dialing a telephone number**: 
```
Dial <a href="tel:+1234567890">my phone number</a>.
```

- 'target="_blank"' attribute in 'a' tag: it opens a new tab when you click on the link.
```
<a href="https://www.google.com/" target="_blank">Google</a> in a new tab.
```

## Chapter6: Add Image 

```
<img src="img/html_logo.jpg" alt="HTML5 Logo" title="I am learning HTML5." width="300">
```

- ```<img>``` tag is to add image to the file
- ```<img src="img/html_logo.jpg">``` - **src** attribute contains the source of the image 
- ```<img src="" alt="HTML5 Logo">``` - **alt** attribute is alternative text, it helps to the assistive technologies for those who may not be able to see the image (a screen reader will read the description). This text is also appears on the page, if the image does not load for some reason. 

- ```<img src="" alt="" title="">``` - **title** attribute, it is not access able, a screen reader will not read it, so it cannot be something very important. This is text, that can complement our image, but not necesseraly required. It is visible when you hover with your mouse to the image. 

- ```width``` attribute: it will tell the width of the image. If we only provide the width, html will automatically match/adjust the heigh of the image. CSS will override these values. 

- ```height``` attribute: tells the height of the image we apply on. CSS will override these values. 

- It is recommended to provide **width** and **height** attributes in the 'img' tag because of the **cumulative layout**, we tell the browser that something needs space here. If we don't provide them, the browser shifts everything.

- ```loading``` attribute: it is set to **"eager"** value by default, but now let's set it to **"lazy"**. Any image that is below the fold (that is what you don't currently see when the page loads), you set the loading attribute to lazy, and that means that the browser will only load that iomage when it knows it is about to show , when we scroll down. Because images are not loaded, it loads the web page faster. It is a good **performance technique**, especially when you are dealing with lots of images. 

- ```figure``` element - we wrap the image tag into this figure element. It doesn't do much by itself, but it intends the image. Add a `figcaption` element to the image, which is basically better than just add a paragraph. Figcaption is a caption under the image. 

```
<figure>
    <img src="img/vacation.jpg" alt="Caribbean beach" title="I want to visit a Caribbean beach as soon as possible." width="400" height="225" loading="lazy">
    <figcaption>Caribbean Beach Holiday</figcaption>
</figure>
```

```
<figure>
    <img src="img/html.jpg" alt="HTML5 Logo" title="I am learning HTML5." width="400" height="225">
    <figcaption>An Example of HTML5 Code: </figcaption>
    <p>
        <code>&lt;h1&gt;Hello World!&lt;/h1&gt;</code>
    </p>
</figure>
```

- Another way to use figure element: it can contain code snippet, and it can have a caption on the top.

## Chapter7: Semantic Tags

- ```h1-h6``` - hierarchy of headers - there is only one ```h1``` tag per page
- you can have multiple `h2` headers which is one level down in the hierarchy, and they are define sub-topics

- **Semantic html tags** help us quickly see or read the different sections in the web page and navigate to those sections. They makes our pages accessible to screen readers and other assistive technology

- ```<nav>``` element is semantic, it contains a grouping of links in our index.html. 

- ```<section>``` element: represents a generic standalone section of a document.

- ```<header>``` element: represents introductory content, usually a heading, navigation, author name, form, etc. It can be more ```header``` in a page. (we include the h1 and nav elements)

- ```<main>``` element: there is only one main per page for the whole content of the page.  (we include our 2 'sections'). 


- ```<footer>``` element: at the botton of the page. 

Now we created 3 sections of our page: **header, main and footer**.  

- we can have more ```<nav>``` elements on one page (one at the top, one at the botton). It is important to label them so the assistive technology knows which nav is which.

    - ```<nav aria-label="primary-navigation">``` - 'aria-label' attribute can help 

- ```<article>``` (change 'section' tags to 'artice') - it clearly has its own topics, it represents a self-contained composition in a page, which is independently reuseable. Example: a forum post, newspaper article... 

- ```<aside>``` element - represents a portion of a document whose content is only indirectly related to the document's main content. Asides are frequently presented as sidebars or call-out boxes, a complementary text that is not as important as what is in the main section

- ```details>``` element - it creates a disclosure widget in which information is visible only when the widget is toggled into an open state. A summary or label must be provided using the ```<summary>``` element.

- ```<mark>``` element - inline element, it highlights the text in the enclosing context. 

- ```<div>``` element - it has no semantic meaning, it is much like a section, you would see a lot in older html code. You should avoid using div in your code. 

#### Download Html5 Outliner from Chrome Web Store 

## Chapter8: Create Tables 

- Tables are made up of rows and columns 
- tr: table row
- th: table header: automatically formatted, centered and bold
- td: table data 

```
<table>
    <thead>
        <tr>
            <th></th>
            <th></th>
            ...
        </tr>
    </thead>
    <tbody>
        <tr> 
            <td></td>
            <td></td>
        </tr>
        <tr> 
            <td></td>
            <td></td>
        </tr>
        ...
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2"></td>
        </tr>

    </tfoot>
</table>
```

- ```<caption>``` semantic tag in table, we cansay what the table is about, it helps to the screen readers 
- ```<thead>``` is the table head
- ```<tbody>``` is the table body
- ```<tfoot>``` is the table foot 