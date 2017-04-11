# Lesson 4: Web Applications

## Objectives
In this chapter students learn how to use HTML and CSS to create web pages, introduction to JavaScript and ASP.NET, and learn the basics of web hosting for the purpose of creating a Web Application.

## Web Concepts
* URL *Uniform Resource Locator* is the short way of saying Website Address, for example: http://www.mywebsite.com
* Every Web Address starts with http:// or https:// (secure)
* The mywebsite.com part is called a DOMAIN NAME, which essentially masks the actual location of a website and makes it easy for us to remember.  Otherwise, websites would be displayed using IP Addresses and folder directories.
* Every device on a Network (The Internet) is given an IP Address, which is similar to a phone number or house address.
* Websites are made up of multiple documents, stored on another computer called a server.  When you visit a website your Web Browser (Chrome, Edge, Internet Explorer, Firefox, etc) sends an HTTP:// request to the server.  The server responds by sending files back to your web browser, and your browser processes the data into something you can see.
* The foundation of any website is built using HTML and CSS.
* HTML stands for HyperText Markup Language and defines the structure of a document, such as image placement, text, headings, tables, etc.  The language itself consists of tags, or angled brackets < />. HTML is CLIENT-SIDE meaning it is rendered by the browser.
* CSS stands for Cascading Style Sheets and is responsible for the Style or Design of a page, such as fonts, colors, animations, and more.  The language uses 'selectors' and curly brackets {} to format web pages.  CSS is CLIENT-SIDE meaning it is rendered by the browser.
* JavaScript is a language that adds interactivity and dynamic content to your website.  Most JavaScript is CLIENT-SIDE, meaning it is rendered by the browser.
* XML is eXtensible Markup Language that makes it easy to store and transport data.  Unlike HTML, XML does not have pre-defined tags - they are all made-up by the document author.  XML is CLIENT-SIDE, meaning its tags are served and rendered on the browser.
* AJAX is a combination of JavaScript and XML that allows the send/request/receive/display of data without reloading a web page.  Ajax is a client-side script that communicates to and from a server/database without the need for a postback or a complete page refresh.
* ASP.NET, PHP, Ruby, and Python are examples of Server-Side Programming Languages.
* IIS, or Internet Information Services, is installed on Windows computers to create and manage web hosting.


# Exercise
1. Open a text-editor such as Notepad or Visual Studio Code
2. Using the code below, create your first web page using HTML
3. Save the document as index.html

```HTML5
<!DOCTYPE html>
<head>
   <title>My Website</title>
   <link rel="stylesheet" type="text/css" href="mystyle.css">
</head>

<body>
   <h1>My Name</h1>

   <div>
      <p>Hello my name is _________ and I am from TAMPA, Florida.</p>
   </div>
   
</body>
```

4. Go to where you've saved index.html and double-click: it should open in your web browser
5. Now lets make another text file.  We will save this one as **mystyle.css**

```HTML5
body
{
  background: black;
}

h1{
  color: red;
}

p {
  text-align: center;
  color: blue;
}


div {
  border: 5px solid grey;
  width: 400px;
  margin: 0 auto;
  background: rgba(255,255,255,.7);
}

```

6. Refresh your web page.  What happened?



## Details
Details about what the code above goes here

* `Each line of code should be bulleted here`
    * A bulleted list of things about the line above should go here
    * **Really important stuff should be bold like this**
    * Keywords should be *italicized*
# Exercise

A challenge relating to the original sample code should go here.