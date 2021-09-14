# Selenium

## XML Document

* XML stands for eXtensible Markup Language
* XML is a markup language much like HTML
* XML was designed to store and transport data
* XML was designed to be self-descriptive

    <note>
      <to>Tove</to>
      <from>Jani</from>
      <heading>Reminder</heading>
      <body>Don't forget me this weekend!</body>
    </note>
  
The XML above is quite self-descriptive:

It has sender information, receiver information, a heading and a message body. But still, the XML above does not DO anything. XML is just information wrapped in tags. Someone must write a piece of software to send, receive, store, or display it.

XML and HTML were designed with different goals:

XML was designed to carry data - with focus on what data is. HTML was designed to display data - with focus on how data looks. XML tags are not predefined like HTML tags are.


The XML language has no predefined tags. The tags in the example above (like <to> and <from>) are not defined in any XML standard. These tags are "invented" by the author of the XML document.
  
## XPath in Selenium
  
XPath in Selenium is an XML path used for navigation through the HTML structure of the page. It is a syntax or language for finding any element on a web page using XML path expression. XPath can be used for both HTML and XML documents to find the location of any element on a webpage using HTML DOM structure.
 
Syntax for XPath selenium:
  
XPath contains the path of the element situated at the web page. Standard XPath syntax for creating XPath is:
  
  Xpath=//tagname[@attribute='value']
  

* // :	Select current node.
* Tagname: Tagname of the particular node.
* @:	Select attribute.
* Attribute:	Attribute name of the node.
* Value:	Value of the attribute.

## Selenium
    
Selenium refers to a suite of tools that are widely used in the testing community when it comes to cross-browser testing. Selenium cannot automate desktop applications; it can only be used in browsers. It is considered to be one of the most preferred tool suites for automation testing of web applications as it provides support for popular web browsers which makes it very powerful.
    
It supports a number of browsers (Google Chrome 12+, Internet Explorer 7,8,9,10, Safari 5.1+, Opera 11.5, Firefox 3+) and operating systems (Windows, Mac, Linux/Unix).
    
## Selenium Components
    
The Selenium test suite comprises four main components:-

* Selenium IDE
* Selenium RC
* Selenium Webdriver
* Selenium Grid

### 1. Selenium IDE
    
Selenium IDE (Integrated Development Environment) is primarily a record/run tool. It is an Add-on or an extension available for both Firefox and Chrome that generates tests quickly through its functionality of record and playback. You don’t need to learn any test scripting language for authoring any functional tests.

### 2. Selenium RC
    
In the case of working with Selenium RC (Remote Control), one must have good knowledge of at least one programming language. This tool allows you to develop responsive design tests in any scripting language of your choice. Server and client libraries are the two main components of Selenium RC. Its architecture is complex and it has its limitations.

### 3. Selenium Webdriver   
    
Selenium WebDriver is an enhanced version of Selenium RC. It was introduced in the market to overcome the limitation faced in Selenium RC. Though it is an advanced version of RC, its architecture is completely different from that of RC. Just like Selenium RC, Selenium WebDriver too supports multiple programming platforms to provide wider flexibility and requires knowing any one programming language.

### 4. Selenium Grid   
    
Selenium Grid is a tool that is used for concurrent execution of test cases on different browsers, machines, and operating systems simultaneously. This tool makes Cross-browser compatibility testing very easy. There are two versions of the Selenium Grid – the older version is known as Grid 1 and the recent version is known as Grid 2.
    
## Selenium Webdriver
    
Selenium WebDriver is a web framework that permits you to execute cross-browser tests. This tool is used for automating web-based application testing to verify that it performs expectedly.

Selenium WebDriver allows you to choose a programming language to create test scripts. As discussed earlier, it is an advancement over Selenium RC to overcome a few limitations. Selenium WebDriver is not capable of handling window components, but this drawback can be overcome by using tools like Sikuli, Auto IT, etc.
    
### Selenium WebDriver Framework Architecture
    
WebDriver Architecture is made up of four major components:
    
* Selenium Client library
* JSON wire protocol over HTTP
* Browser Drivers
* Browsers    

<img src="Images/SeleniumWebDriverArchitecture.png">    
