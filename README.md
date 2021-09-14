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

