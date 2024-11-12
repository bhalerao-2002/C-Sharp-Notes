# Defect Life Cycle: 
- Defect life cycle, also know as Bug Life Cycle is the journey of a defect cycle, which a defect goes through during its lifetime.
 ![image](https://github.com/user-attachments/assets/a9418dd6-65c2-4186-a306-354ac2eb3eed)

- New : New defect that is raised and yet to be validated.
- Assigned : The defect is then assigned against a development team to address it but not yet resolved.
- Active : The defect is begin addressed by the developer and investigation is under progress. At this stage there are two possible outcomes;
  1. Deferred:- When a defect cannot be addressed in that particular cycle it is deferred to future release.
  2. Rejected:- A defect can be rejected for any of the 3 reasons
     a. Duplicate defect, 
     b. Not a defect, 
     c. Non Reproducible.
- Test:- The Defect is fixed and ready for testing.
- Reopened:- When he defec is NOT fixed, QA reopens/reactivates the defect.
- Verified:- The Defect that is retested and the test has been verified by QA.
- Closed :- The final state of the defect that can be closed after the QA retesting or can closed if the defect is duplicate or considered as Not defect.
 
###  Defect triage:
Defect triage is a process of evaluating and prioritizing defects or bugs based on their severity, impact, and likelihood of occurrence. It involves a team of stakeholders, including developers, testers, project managers, and other relevant personnel, who come together to review, analyse and prioritize defects.

The goal of deefect triage is to ensure that critical defects are addressed promptly, while less severe defects are resolved in a timely manner, and resoursces are allocated effectively.

### Defect Prioritization: 

Defect prioritization is the process of ranking or categorizing sofware defects or bugs based on their impact and severity. 
It is an essential step in defect mangement, as it helps the development team to identify the most critical issues that need to be resolved first.

### Defect Tracking:

Defect tracking is the process of identifying, documenting, and managing software defects or bugs throughout the software development lifecycle. It involves tracking the defect from the time they are reported until they are resolved and verified.

In defect tracking, each defect is assigned a unique identifier and is entered into a tracking system, such as a defect tracking tool. The system is used to capture and manage information related to the defect, including its severity, priority, steps to reproduce, and the status of its resolution

### Defect report?
A defect report is a document that describes a software defect or bug that has been identified during the testing or development phase of a software project. It is typically created by a tester or QA engineer and is used to report the details of the defect to the development team for further investigation and resolution.

### Defect leakage?
Defect leakage, also known as "escape defects," refers to the situation where a software defect that was previously identified and reported is not completely fixed and is released into the production environment. It means that a defect has escaped from the testing process and has been released into the live environment where end-users can encounter it.

### Defect report template and the purpose of a defect report template?
- A defect report template is a pre-designed format used to document and report  software defects.
- It includes details such as **defect ID, summary, description, severity, priority, status, assignee, reporter, and dates reported and fixed**.
- The purpose is to provide a standardized format for tracking defects, ensuring all necessary information is captured, and facilitating effective communication among different teams.

### Ddefect trend analysis and the purpose of defect trend analysis?
- Defect trend analysis is the process of analyzing data on defects over time to identify patterns or trends and make data-driven decisions to improve the software development process.
- The purpose of defect trend analysis is to identify the frequency, severity, and types of defects that are occurring, as well as their root causes, so that corrective actions can be taken to prevent similar issues from occurring in the future. By analyzing data on defects over time, teams can identify areas where improvements are needed and take proactive steps to address issues before they become larger problems.

### Defect removal efficiency?
Defect Removal Efficiency (DRE) is a metric used to measure the effectiveness of the  testing process in detecting and removing defects or bugs from software. DRE is calculated as the percentage of defects that were found and fixed during the testing process, compared to the total number of defects in the software.

The formula for calculating DRE is:

**DRE = (Total defects - Defects found and fixed during testing) / Total defects x 100%**

For example, if there were a total of 100 defects in the software, and 80 were found and fixed during testing, the DRE would be:

DRE = (100 - 80) / 100 x 100% = 20%

This means that the _**testing process was able to find and fix 80% of the defects**_ in the software, resulting in a DRE of 20%.

### Defect acceptance rate?
Defect acceptance rate is the percentage of defects found during testing that are accepted by the development team as valid issues. It measures the effectiveness of the testing process in identifying and reporting real issues, and is calculated by 

**DAR = (no. of accepted defects) / (total no. of defects found during testing)**

A higher defect acceptance rate indicates better communication and collaboration between the testing and development teams.

### Defect triage board and the purpose of a defect triage board?
A defect triage board is a visual tool used by **testing and development teams** to prioritize and manage defects throughout the life cycle. Its purpose is to provide a central location where all defects are tracked and visible to the team, allowing for collaboration and communication. It helps prioritize defects based on their impact on the system and allocate resources efficiently to address critical defects promptly.

  
1. Selenium
- Think of Selenium as your "robot tester"
- It automates web browser actions (clicking buttons, filling forms, etc.)
- It's like having someone who can test websites super fast without getting tired

2. Gradle
- Think of Gradle as your "project organizer"
- It manages your project dependencies (external tools/libraries you need)
- It helps build and run your project smoothly
- It's like a manager who makes sure everyone has the tools they need

3. Cucumber
- Think of Cucumber as your "translator"
- It turns plain English test scenarios into code
- It helps non-technical people understand test cases
- It's like a bridge between business people and developers

How they work together:
- Cucumber writes the recipe (test cases)
- Selenium does the cooking (test execution)
- Gradle makes sure the kitchen has all ingredients and tools (project management)

Real example:
```
1. Cucumber (The Plan):
   Feature: Login functionality
   Scenario: User logs in with valid credentials
   Given user is on login page
   When user enters username and password
   Then user should see dashboard

2. Selenium (The Action):
   - Actually opens the browser
   - Finds the login form
   - Types the credentials
   - Clicks the login button
   - Verifies the dashboard appears

3. Gradle (The Support):
   - Makes sure Selenium and Cucumber are installed
   - Manages their versions
   - Runs the tests when needed
   - Handles any other required dependencies
```

Why they're important to each other:
1. Cucumber needs Selenium to execute the actual test actions
2. Selenium needs Gradle to be properly installed and managed
3. Gradle helps Cucumber and Selenium work together smoothly

This combination creates a powerful automated testing framework that is:
- Easy to understand (thanks to Cucumber)
- Reliable in execution (thanks to Selenium)
- Well-organized and maintainable (thanks to Gradle)
