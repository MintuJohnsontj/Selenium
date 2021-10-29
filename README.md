# Selenium Webdriver

[Selenium-python](https://selenium-python.readthedocs.io/installation.html)
    
Selenium refers to a suite of tools that are widely used in the testing community when it comes to cross-browser testing. Selenium cannot automate desktop applications; it can only be used in browsers. It is considered to be one of the most preferred tool suites for automation testing of web applications as it provides support for popular web browsers which makes it very powerful.
    
It supports a number of browsers (Google Chrome 12+, Internet Explorer 7,8,9,10, Safari 5.1+, Opera 11.5, Firefox 3+) and operating systems (Windows, Mac, Linux/Unix).
    
Selenium WebDriver is a web framework that permits you to execute cross-browser tests. This tool is used for automating web-based application testing to verify that it performs expectedly.

Selenium WebDriver allows you to choose a programming language to create test scripts. It is an advancement over Selenium RC to overcome a few limitations. Selenium WebDriver is not capable of handling window components, but this drawback can be overcome by using tools like Sikuli, Auto IT, etc.
    
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
    
When a page is loaded by the browser, the elements within that page may load at different time intervals. This makes locating elements difficult: if an element is not yet present in the DOM, a locate function will raise an ElementNotVisibleException exception. Using waits, we can solve this issue. Waiting provides some slack between actions performed – mostly locating an element or any other operation with the element. Selenium Webdriver provides two types of waits – implicit & explicit.     
    
### 1. Implicit wait
    
Based on time
 
### 2. Explicit wait  

There are some convenience methods provided that help you write code that will wait only as long as required. Explicit waits are achieved by using webdriverWait class in combination with expected_conditions.

    element = WebDriverWait(driver, 10).until(EC.presence_of_element_located((By.ID, "myDynamicElement"))
        
This waits up to 10 seconds before throwing a TimeoutException unless it finds the element to return within 10 seconds. WebDriverWait by default calls the ExpectedCondition every 500 milliseconds until it returns successfully.

#### Expected Conditions
There are some common conditions that are frequently of use when automating web browsers. For example, presence_of_element_located, title_is, ad so on. one can check entire methods from here – Convenience Methods. Some of them are –

* title_is
* title_contains
* presence_of_element_located
* visibility_of_element_located
* visibility_of
* presence_of_all_elements_located
* text_to_be_present_in_element
* text_to_be_present_in_element_value
* frame_to_be_available_and_switch_to_it
* invisibility_of_element_located
* element_to_be_clickable
* staleness_of
* element_to_be_selected
* element_located_to_be_selected
* element_selection_state_to_be
* element_located_selection_state_to_be
* alert_is_present

    
## Selenium vs Scrapy
 
[Framework comparisson](https://www.accordbox.com/blog/web-scraping-framework-review-scrapy-vs-selenium/)

The two Python web scraping frameworks are created to do different jobs. Selenium is only used to automate web browser interaction, Scrapy is used to download HTML, process data and save it.

### Javascript

We should use some tool such as Dev Tool from Chrome to help us figure out how the data is displayed on the dynamic page of target site. If the data is included in html source code, both frameworks can work fine and we can choose one as we like. But in some cases the data show up after many ajax/pjax requests, the workflow make it hard to use Scrapy to extract the data. If it faced with this situation, it is recommended to use Selenium instead.  

### Data Size

Before coding, we need to estimiate the data size of the extracted data, and the urls need to visit. Scrapy only visit the url you told him, but Selenium will control the browser to visit all js file, css file and img file to render the page, that is why Selenium is much slower than Scrapy when crawling.

If the data size is big, Scrapy is the better option because it can save you a lot of time and time is a valuable thing.

### Extensibility

The architecture of Scrapy is well designed, we can easily develop custom middleware or pipeline to add custom functionality. Scrapy project can be both robust and flexible. After developing several Scrapy projects, we will benefit from the architecture and like its design because it is easy to migrate from existing Scrapy spider project to another one.

So if the project is small, the logic is not very complex and want job done quickly, we can use Selenium to keep your project simple. If the project needs more customization such as proxy, data pipeline, then the Scrapy might be the choice here.
       
## Running Selenium Webdriver with a proxy

[tutorialspoint.com](https://www.tutorialspoint.com/running-selenium-webdriver-with-a-proxy-in-python)

We can run a proxy with Selenium webdriver in Python. A proxy is an essential component to do localization testing. We can take an e-commerce application and check if the language and currency visible is as per the user location.

With the help of proxy within tests, we can verify if the website user interface matches with the location. We have to SET a proxy with below steps −

* Import webdriver from Selenium package.

* Define proxy server address.

* Create an object of ChromeOptions class

* Communication of proxy with ChromeOptions.

* Summing options to Chrome() object.

Code Implementation:

        from selenium import webdriver
        #proxy server definition
        py = "128.21.0.0:8080"
        #configure ChromeOptions class
        chrome_options = WebDriverWait.ChromeOptions()
        #proxy parameter to options
        chrome_options.add_argument('--proxy-server=%s' % py)
        #options to Chrome()
        driver = webdriver.Chrome(chrome_options= chrome_options)
        driver.implicitly_wait(0.6)
        driver.get("https://www.tutorialspoint.com/index.htm")
        
Then, to check if a search field has the present user address we shall add the below code snippet:

        def checkL(self):
            self.driver.get(self.url)
            st = self.driver.find_element_by_xpath('#loc')
            #check location with assertion
            self.assertEqual('India', st.text)        

If we have to verify more than locations, we can create a method and pass the proxy address as an argument.

## Add custom HTTP headers

[Add custom HTTP headers in Selenium Webdriver tests in Python in four simple steps](https://webelement.click/en/four_simple_steps_to_add_custom_http_headers_in_selenium_webdriver_tests_in_python)

