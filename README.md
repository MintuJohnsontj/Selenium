# Selenium

[Selenium-python](https://selenium-python.readthedocs.io/installation.html)

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

#### 1. Selenium Client Libraries/Language Bindings    
    
Selenium provides support to multiple libraries such as Ruby, Python, Java, etc as language bindings have been developed by Selenium developers to provide compatibility for multiple languages. For instance, if you want to use the browser driver in Python, use the Python Bindings. You can download all the supported language bindings of your choice from the official site of Selenium.    

#### 2. JSON Wire Protocol   

JSON is an acronym for JavaScript Object Notation. It is an open standard that provides a transport mechanism for transferring data between client and server on the web. It provides support for various data structures like arrays and objects which makes it easier to read and write data from JSON.

JSON serves as a REST (Representational State Transfer) API that exchanges information between HTTP servers.
    
#### 3. Browser Drivers  
    
Selenium provides drivers specific to each browser and without revealing the internal logic of browser functionality, the browser driver interacts with the respective browser by establishing a secure connection. These browser drivers are also specific to the language which is used for test case automation like C#, Python, Java, etc.

You can download the browser driver of your choice as per your language requirements. For example, you can configure Selenium Web driver for Python on BrowserStack.    
    
When a test script is executed with the help of WebDriver, the following tasks are performed in the background:
    
* An HTTP request is generated and it is delivered to the browser driver for every Selenium Command
* The HTTP request is received by the driver through an HTTP server
* All the steps/instructions to be executed on the browser is decided by an HTTP server
* The HTTP server then receives the execution status and in turn sends it back to the automation scripts
    
#### 4. Browsers

As discussed earlier, Selenium provides support for multiple browsers like Chrome, Firefox, Safari, Internet Explorer etc.    
    
## Basic Steps in a Selenium WebDriver Script 
    
* Create a WebDriver instance.
* Navigate to a webpage.
* Locate a web element on the webpage via locators in selenium.
* Perform one or more user actions on the element.
* Preload the expected output/browser response to the action.
* Run test.
* Record results and compare results from them to the expected output.

In order to run tests, one must be familiar with the Basic Commands in Selenium WebDriver.    

## How Selenium WebDriver Works?   
    
On a high-level, Selenium WebDriver works in three steps:
    
* Test commands are converted into an HTTP request by the JSON wire protocol.

* Before executing any test cases, every browser has its own driver which initializes the server.
    
* The browser then starts receiving the request through its driver.
 
    
        exec_path = "C:/Users/user1/Downloads/chromedriver_win32/chromedriver.exe"

        driver = webdriver.Chrome(options = options, executable_path = exec_path)

        driver.get("https://www.techwithtim.net/")
    
As soon as you complete writing your code, execute the program. The above code will result in the launching of the Chrome browser which will navigate to the BrowserStack website.
    
Now let us understand what goes behind the scene when you click on Run until the launching of the Chrome Browser.

Once the program is executed, every line of code/script will get transformed into a URL. The JSON Wire protocol over HTTP makes this possible. Then this URL is passed to the browser drivers (in our example, the ChromeDriver). At this point, our client library (Python in our example) translates the code into JSON format and interacts with the ChromeDriver.
    
Now let us understand what goes behind the scene when you click on Run until the launching of the Chrome Browser.

Once the program is executed, every line of code/script will get transformed into a URL. The JSON Wire protocol over HTTP makes this possible. Then this URL is passed to the browser drivers (in our example, the ChromeDriver). At this point, our client library (Python in our example) translates the code into JSON format and interacts with the ChromeDriver.
    
The URL after JSON conversion looks as follows:
    
    https://localhost:8080/{"url":"https://www.techwithtim.net/"}
    
To receive the HTTP requests, every Browser Driver uses an HTTP server. Once the browser driver receives the URL, it processes the request by passing it to the real browser over HTTP. And then all your commands in the Selenium scripts will be executed.
    
Types of Requests:

There are two types of requests you might be familiar with – GET and POST.

If it’s a GET request then it results in a response that will be generated at the browser end and it will be sent over HTTP to the browser driver and eventually, the browser driver with the help of JSON wire protocol sends it to the UI (Eclipse IDE).    
    
## Algorithm 
   
### Step 1: Create a WebDriver instance
        
        PATH = "/home/user1/Downloads/chromedriver_linux64/chromedriver"
        driver = webdriver.Chrome(PATH)
        driver.get("https://www.techwithtim.net/")
        print(driver.title)
        
### Step 2: Navigate to the required web page and locate a web element on the webpage via locators in selenium   
    
        search = driver.find_element_by_name("s")
    
### Step 3: Perform one or more user actions on the element
    
        search.send_keys("python")
    
## Synchronization & Waits
    
### 1. Implicit wait
    
    Based on time
 
### 2. Explicit wait  
    
    
