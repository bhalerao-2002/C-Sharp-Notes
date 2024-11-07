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

