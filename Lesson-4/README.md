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

## Details


* `<!DOCTYPE html>`
    * Document Type declaration, indicates to the web browser that this is an HTML document.
    
* `<head> </head>`
    * Anything between the head tag is usually related to stylesheets being applied to a page or setting the title for the tab.
 
 * `<body> </body>`
   * Text and tags between the body tags are part of the page content - the stuff people actually see on your page.
   
 * `<h1> </h1>`
   * Heading tags designate sections of text with larger or accented text.
   * Heading tags run h1-h6, with h1 being the largest.
   
 * `<div> </div>`
   * Div is short for divider.  A div can be put around content that needs to be styled specifically.
    
 * `<p> </p>`
   * Paragraph tags surround text that should be spaced as if it belongs in a separate paragraph.  Easy enough.
    
    

# Exercise

4. Go to where you've saved index.html and double-click: it should open in your web browser
5. Now lets make another text file.  We will save this one as **mystyle.css**
6. Refresh your web browser page when you are done.  What happened?

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

* CSS
   * Cascading Style Sheets are written a little differently, using a selector and curly brackets.
   * Think of styling as using Microsoft Word.  For example, when you want to change the color of a font, you first **select** the text you'd like to change, then choose the paint bucket icon, and pick a color. Since we cannot drag our mouse to highlight stuff and expect that to translate to code, we have to tell the web browser what to do using text.  
   * When we want to change the color of text between an `<h1> </h1>` tag, we clearly specify **h1** and follow it with curly brackets **{ }**  
   * Inside the curly brackets you should put all changes you'd like to see made to the text between those **h1** tags, such as color, background, font, and more.
   
* `body {}`
    * Targets the web page itself.  Great for setting an overall background color to the page
    
* `{ background: black; }`
   * Inside the curly brackets we should put all changes we'd like to a particular selector.  
   * Each change is indicated like so **Property: Attribute;**
   * Colons (:) go after each Property.  Properties are keywords, in which there are many to learn!
   * Semicolons (;) should end each line and come after the attribute.  Some attributes have tricky formatting, but usually it's just one word.
   
* `h1 {color: red;}`
   * Changes all h1 tags to have red color font
   
* `p {text-align: center; color: blue;}`
   * **Usually you should hit the enter key after each semicolon (;), but for the purpose of this section we will place the properties on one line.**
   * Paragraph font color is blue
   * Paragraph text is centered on the page
   
* `div {border: 5px solid grey; width: 400px; margin: 0 auto; background: rbga(255,255,255,.7); }`
   * Divider receives a border around it that is 5 pixels wide, a solid line (could be dashed, dotted, etc), and is colored grey.
   * The divider spans a width of 400 pixels on the page.
   * The top and bottom margin is 0 and the sides automatically adjust to center the divider on the page.
   * The background is using an RGBA format.  The values for RED, GREEN, and BLUE could range from 0-255.  The last digit is ALPHA, or opacity, which is a value between 0-1 (think percentage, or decimal).

    
# Exercise
1. Next we will explore how JavaScript can make our pages interactive and dynamic.  
2. Open another text-editor document and save it as SampleScript.js
3. Enter the code below.  When you are done save your JavaScript file.

```JavaScript
username = prompt("Please enter your name");
message = "Hello, " + username + ". Your name has ";
nameLen = username.length;

if (nameLen > 5) 
   message = message + "more than ";
else if (nameLen < 5)
   message = message + "less than";
else
   message = message + "exactly";
 message = message + "5 characters.";
 alert(message);
 ```
 ## Continue exercise...
 
 4. In order for our JavaScript file to do anything we must "call it" within our web page.
 5. With your text-editor, open your index.html file that was created earlier.
 6. Add the script to your head tag, like shown:
 
 ```JAVASCRIPT
<head>
   <title>My Website</title>
   <link rel="stylesheet" type="text/css" href="mystyle.css">
   <script src="Sample.js"></script>
</head> 
 ```

* **JavaScript** 
   * is a client-side scripting language that is interpreted by the web browser.  In contrast, C# is compiled by an IDE.
   * All JavaScript code or source links should be placed within **script** tags.  Usually script tags are placed in the head, but not always.
   * Not all users or web browsers have JavaScript enabled.  You may want to include a `<noscript>` element to deliver a message to these clients.
 
 
 # Exercise (Optional)
 ### Install and Configure IIS on a Windows 10 Computer
 IIS or Internet Information Services is used to setup a web host on a Windows Server.  After this exercise you will be able to access your website by typing localhost into your web browser.  It will not be mapped to a domain or live on the internet for others to see - you would require a dedicated IP address for this to work outside of your local network.
 1. You must be logged in as an Administrator and on Windows 10 Operating System
 2. Go to Cortana to Search Windows and type: Programs and Features
 3. In the sidebar click "Turn Windows Features On/Off"
 4. Check the box next to Internet Information Services
 5. Expand (+) Internet Information Services
 6. Expand (+) Application Dev. Features
 7. Check CGI
 8. Click OK and Wait.
 9. Open your C:\ drive and double-click inetpub folder
 10.  You should have a wwwroot folder - this is your main website directory.  Move your index.html, mystyle.css, and Sample.js files here.
 11. Open IIS (you can do a Windows Search for Internet Information Services)
 12. In the left sidebar, expand "Sites" and Right-Click **Default Web Site** -> **Edit Permissions**
 13. Go to the Security Tab and "ALLOW" everything on your Administrator's Account.
 14. On the right sidebar you should have an option to **START** the web server.
 15. Open your web browser and type: **localhost** 
 
 *If you were to setup a domain (.com) you could go to EDIT BINDINGS on the right sidebar.*

Feel free to explore this area.
 
 
 ### Web Applications and Web Services are Server-Side Programming
* **ASP.NET** allows you to create applications that completely execute on the server. 
   * This is part of the .NET Framework, which enables you to develop programmable Web forms and Web Services.
   * You can develop .NET applications in any language compatible with the .NET common language runtine such as Visual Basic and C#
* **AJAX** applications use a mixture of JavaScript and XML to provide fast, responsive interfaces while storing data.

### When you visit an ASP.NET web page an HTTP request is sent to the server and the web server executes a process:
1. The Internet Information Service (IIS) receives the HTTP request to retrieve an ASP.NET page
2. IIS loads a file called aspnet_isapi.dll which starts the worker process: aspnet_wp.exe
3. The worker process compiles the .aspx file into a Common Language Runtime (CLR) to execute the assembly
4. When the assembly executes, classes in the .NET Framework library perform their tasks and generate a response message for the requesting client.
5. The ASP.NET worker process collects the response(s) generated by the execution of the web page and passes it back to the  aspnet_isapi.dll process
6. Aspnet_isapi.dll forwards the response to IIS which is then turned over to the web page client computer.

**Prior to execution each ASP.NET page is converted into a class.  The class derives most of its functionality from the System.Web.UI.Page class, which provies properties such as: Request, Response, Session, and Server**


## Example:
In a typical contact form, after you enter information and hit the submit button, the page can process the submitted data to take an ACTION.  The action might be to submit to a database or send an email.  A **POSTBACK** occurs, which may appear to load the same page over again, but is actually submitting the data by posting back to the same web page for processing.  Other times the page may process and post a Thank You message to a new page as confirmation.
