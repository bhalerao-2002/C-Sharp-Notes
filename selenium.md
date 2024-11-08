# Selenium: 
- Selenium is a set of open-source web automation tools that leverages the power of web browsers and helps automate workflows of how users interact with the web application within the browser

### Selenium Advantages:
- Open-source tool
- Extended for various technologies.
- Capabilities to execute scripts across different browsers.
- Execute scripts on various operating systems.
- Supports mobile devices.
- Can execute tests in parallel with the use of Selenium Grids.

### Selenium Disadvantages:
- Supports only web based applications.
- No feature such as Object Repository/Recovery Scenario
- No IDE, so the script development won't be as fast as QTP.
- Cannot access controls within the browser.
- No default test report generation.
- For parameterization, users has to rely on the programming language.

## Components of Selenium:
![image](https://github.com/user-attachments/assets/20e29617-c827-452e-996f-f2316db5f38d)
- Selenium IDE
  - It is an extension available for browsers, which has the record and replay functionality available.
- Selenium RC
  - It is a server that acts as a middleman between the user and the browser that needs to interact. It had issues with the **One Origin Policy** and was deprecated in favor of WebDriver.
- Selenium WebDriver
  - WebDriver allows users to write custom code in their language of choice and interact with the browser of their choice, through browser-specific drivers. WebDriver works on the OS level and uses a Protocol called **JSONWireProtocol** to communicate with browsers.
- Selenium GRID
  - It allows users to run tests on different machines, with different browsers and OS simultaneously, which gives the ability to run tests in parallel, as such saving a lot of time and resources testing on several machines.
 
## Which Selenium Testing tool fits your need?
- Selenium IDE
  - If you want to learn about automation testing and Selenium.
  - If you have little or no prior experience in test automation.
  - In case you want to write simple test cases and export them later for RC or WebDriver.
  - If you want to execute customized JavaScript code using runScript
  - If you want to export the script in various languages.
  - In case you want to target Chrome and Firefox for testing.
- Selenium RC
  - If you want to write test cases in more expressive language than IDE.
  - If you want to test the application against a new browser that supports JavaScript.
  - Or, if you want to test an application, that is AJAX heavy.
- Selenium WebDriver
  - If you want to use a specific programming language for your automation test cases.
  - If you want to test applications in different platforms using Selenium Grid
  - Or, if you want to test applications in CI/CD.
  - If you want to test applications and generate customized HTML formatted reports.
  - If you want to test modern dynamic data-heavy websites.
- Selenium GRID
  - If you want to run your automation test cases in different browsers and operating systems simultaneously.
  - If you want to run a vast test suite and want to minimize the execution time.
 

# Selenium WebDrivers
- Selenium WebDriver is a set of open-source APIs, which provided the capabilities to interact with any of the modern web-browsers and then, in-turn to automate the user actions with that browser.
- Selenium WebDriver is a component of the Selenium family. It’s the introduction in the system lead to overcome a few of the shortcomings of Selenium RC.
- Selenium WebDriver is a set of APIs, which makes the interaction and actions on the browser very easy and quick.
- Selenium WebDriver provides quite a few unique features, such as it can automate dynamic web pages. Additionally, it can automate all the web applications, no matter in which programming language we use to develop them.
- Selenium WebDriver interacts with the browsers with the help of various drivers provided by corresponding Vendors.


## Why Selenium WebDriver is popular?
- Multi-Browser Compatibility.
- Multi-Language Support
- Faster Execution
- Locating Web Elements
- Handling dynamic web elements.
  - Absolute Xpath
  - Contains()
  - Starts-With()
- Handling Waiting for Elements 

## What are the drawbacks of Selenium WebDriver?
- Requires Programming Knowledge and Expertise
- No Support for Desktop Applications
- No Customer Support
- No Built In Object Repository
- Lack of built-in reporting
- Managing Browser-Selenium Dependencies

## Selenium WebDriver Architecture
![image](https://github.com/user-attachments/assets/b714e3b4-a810-4ebe-a463-e100d880ec48)

## How Selenium WebDriver works?
![image](https://github.com/user-attachments/assets/e1f441fe-9b6f-47ce-b70c-01d508b750c4)
When a user writes a WebDriver code in Selenium and executes it, the following actions happen in the background –
- An HTTP request generates, and it goes to the respective browser driver (Chrome, IE, Firefox). There is an individual request for each Selenium command.
- The browser driver receives the request through an HTTP server.
- The HTTP server decides which actions/instructions need to execute on the browser.
- The browser executes the instructions/steps as decided above.
- The HTTP server then receives the execution status and then sends back the status to an automation script, which then shows the result ( as passed or an exception or error).


### Basic Script of Selenium WebDriver in JAVA


Task we intended to perform in this script is:
- Firstly, open the browser.
- Secondly, navigate to the ToolsQA Demo Website.
- Thirdly, maximize the browser window.
- After that, retrieve the title of the page.
- Fifthly, log in to the Website by specifying credentials.
- Sixthly, validate the LogOut button is visible.
- Lastly, we logout from the Website.

Code:
```
package WebDriversBasics;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class launch {
    public static void main(String[] args) {
//        1. open the browser.
        System.setProperty("webdriver.chrome.driver", "C:\\Users\\ramerus\\Downloads\\chromedriver-win64\\chromedriver.exe");
        WebDriver RushiDriver = new ChromeDriver();

//        2. navigate to the ToolsQA Demo Website.
        RushiDriver.get("https://demoqa.com/login");

//        3. maximize the browser window.
        RushiDriver.manage().window().maximize();

//        4. retrieve the title of the page.
        String title = RushiDriver.getTitle();
        System.out.println("The page title is: " + title);

//        5. log in to the Website by specifying credentials.
        WebElement uName = RushiDriver.findElement(By.xpath("//*[@id='userName']"));
        WebElement pswd = RushiDriver.findElement(By.xpath("//*[@id='password']"));
        WebElement loginBtn = RushiDriver.findElement(By.xpath("//*[@id='login']"));

        uName.sendKeys("testuser");
        pswd.sendKeys("Password@123");
        loginBtn.click();

//        6. validate the LogOut button is visible.
//        7. we logout from the Website.
        try{
            WebElement logoutBtn = RushiDriver.findElement(By.xpath("//div[@class='text-right col-md-5 col-sm-12']//button[@id='submit']"));

            if(logoutBtn.isDisplayed()){
                logoutBtn.click();
                System.out.println("LogOut Success 😊");
            }
        }
        catch (Exception e){
            System.out.println("Ahhh...😒");
        }
//        8. Close the Browser
        RushiDriver.quit();
    }
}
```

# WebDriver Commands

## Browser Commands in Selenium WebDriver:
driver._______
#### A. Basic
1. get(String arg0): void
  1. It opens the URL provided as String.
2. getTitle(): String
  1. Returns title of the Webpage.
3. getCurrentUrl(): String
  1. Returns the current URL which is opened in the browser.
4. getPageSource(): String
   1. Returns the source code of the page.
5. close(): void
  1. Close only the current Window the WebDriver is currently controlling. 
6. quit(): void
   1. Closes all windows opend by the WebDriver.

#### B. Intermediate

#### C. Advanced

## Browser Navigation Command
driver.navigate().________
1. to(String arg0) : void
   1. Loads new web page(provided url) in current browser window
2. forward() : void
   1. This method does the same operation as clicking on the Forward(Next) Button of any browser
3. back() : void
   1. This method does the same operation as clicking on the Back Button of any browser.
4. refresh() : void
   1. This method Refresh the current page.
  

## WebElement Commands
WebElements are HTML elements.
So, to get the WebElement object write the below statement:
```WebElement Rushielement = driver.findElement(By.id("UserName"));```
Rushielement.___________
1. clear( ) : void
   1. If the element is text(input/textarea) entry element, it will clear the value, else it will do nothing.
2. sendKeys(String ) : void
   1. It simulates typing into a element.
3. click( ) : void
   1. Simulates the clicking of any element.
4. isDisplayed( ) : boolean
   1. determines is the element is curretly displayed
5. isEnabled( ) : boolean
6. isSelected( ) : boolean
7. submit( ) : void
   1. It works better than click() on form like elements
8. getText( ) : String
   1. Fetch the visible (i.e. not hidden by CSS) innerText of the element.
9. getTagName( ) : String
   1. gets tag name of elements.
10. getCssvalue( ) : String
11. getAttribute(String Name) : String
12. getSize( ) : Dimension
   1. fetch the width and height of the rendered element
13. getLocation( ) : Point
    1. locate the location of the element on the page.

## Find elements using Selenium WebDriver?
-  to locate or find the elements each method uses a locator strategy which is provided via an argument to the "By" object. These strategies are by Id, by Name, by Class Name, by XPath, by link, etc
  
![image](https://github.com/user-attachments/assets/540dcecf-8bb9-4db0-b445-fbac9283bbb2)

## How to find elements in Selenium?
1. findElement() ->  finds the first most element within the web page, if not found throws the "NoSuchElementException".
2. findElements() -> finds a list of web elements on the web page, if not found doesn't throws the error, simply gives empty list.


## How to handle a CheckBox/radio in Selenium WebDriver?
Locate and select a CheckBox/radio in Selenium using:-
1. ID Locator - driver.findElement(By.id("hobbies-checkbox-1")).click();
2. XPath locator - driver.findElement(By.xpath("//label[text()='Sports']")).click();
3. CSS Selector locator - driver.findElement(By.cssSelector("label[for='hobbies-checkbox-1']")).click();
   
### Validations on a CheckBox/radio: 
isSelected(): Checks whether a CheckBox/radio is selected or not.
isDisplayed(): Checks whether a CheckBox/radio displays on the web page or not.
isEnabled(): Checks whether a CheckBox/radio is enabled or not

## How to handle a DropDown in Selenium WebDriver?
In HTML dropdown is generally implemented using <select> or <input> tag. For hadling DropDown Selenium WebDrivers provides a class called "Select" class.
```Select select = new Select(WebElement webelement);```

### How to select a value from a dropdown in Selenium?
1. selectByIndex(int arg0) : void
   1. It accepts the index of the dropdown value, which needs to be selected. The index starts at 0.
2. selectByValue(String arg0) : void
3. selectByVisibleText(String arg0): void

### How to check whether dropdown is Multi-Select?
isMultiple(): boolean

### How to get options from a dropdown in Selenium?
1. getOptions(): List<WebElement>
2. getFirstSelectedOption(): WebElement
3. getAllSelectedOptions():List<WebElement>

### getAllSelectedOptions():List<WebElement>
1. deselectAll(): void
2. deselectByIndex(int arg0): void
3. deselectByValue(String arg0): void
4. deselectByVisibleText(String arg0): void

## Handle Dynamic WebTables in Selenium Webdriver :
```/html/body/div[1]/div[2]/div/div[2]/article/div/table/tbody/tr[2]/td[1]```
- Part 1 - Location of the table in the webpage </html/body/div[1]/div[2]/div/div[2]/article/div/>
- Part 2 - Table body (data) starts from here <table/tbody/>
- Part 3 - It says table row 2 and table column 1 <tr[2]/td[1]>

# Inspectors Tools & Locators
## Best Practices For Selenium Locators
1. Do not use dynamic attribute values to locate elements, as they may change frequently and result in breakage of locator script. It also severely affects the maintainability, reliability, and efficiency of the automation script.
2. ID and name attributes take precedence over other locators if your web page contains unique ID and name, then it's always advisable to use them instead of XPath as they are faster and more efficient.
3. While using locators, make sure that your locator points precisely to the required element. If the needed scenario needs to perform some operation on a single element, then make sure that your locator exactly matches to only one element. If the locator points to several different elements, then it may cause breakage in your script.
4. Never use locators to locate auto-generated elements on the web page. Sometimes in a dynamic web environment, element attribute properties are generated at run time. One should avoid these elements as they may cause breakage during script execution.
5. While working with XPath or CSS locators, one should avoid directly using the one generated by the Chrome Dev Tools. It may seem one of the easiest ways to generate XPath, but in the long run, it induces reliability issues, code breakage, maintainability issues, etc. It may look tempting to use these, but you would be better off creating your customized XPath in the longer run.

## What is XML Path(Xpath)?
Xpath is a language that describes a way to locate and process items in Extensible Markup Language(XML) documents by using an addressing syntax based on a path through the document's logical structure or hierarchy.
Xpath is used in Selenium to uniquely identify an element on a Webpage as an element locator just like the way we use PostCode and House address in real-world locate the Home Address.

### Syntax of XPath
![image](https://github.com/user-attachments/assets/a0f16c79-d68f-4fd9-92dc-e4ca2f4f82e2)

1. The XPath syntax generally starts with “//” double slash. That is to say, it will begin with the current node defined by the tag name.
2. The next part is tag_name; it denotes the HTML tag name of the node.
3. Subsequently, anything present inside the node encloses in the square brackets.
4. Additionally, the “@” sign selects the attribute.
5. Moreover, the “Attribute_name” is the name of the attribute of the node.
6. And, the “Value of attribute” denotes the attribute value from the node.

### How to locate web elements using XPath in Selenium?
![image](https://github.com/user-attachments/assets/449cc69f-d7ce-4c75-880a-b2b961375871)

### How to locate web elements using Predicates?
![image](https://github.com/user-attachments/assets/72cfeadb-ee9f-4943-a7ea-0545e3f53b18)

### Types of Xpath:
1. Absolute Xpath -> It is direct way of finding the element, e.g., /html/body/div/header/a/img
2. Relative Xpath -> It starts for any node inside the HTML DOM, e.g., //img[@src = "/images/Toolsqa.jpg"]

### XPath Functions 

## CSS Selectors in Selenium
- different ways to create CSS Selectors
  ![image](https://github.com/user-attachments/assets/5b866626-76dc-4ab9-adf3-1afaff35b02f)


# Alerts & Windows:

## Wait in Selenium : 



