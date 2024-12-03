# Testing Interview Questions

## Test Cases Design Techniques  
  
1. Boundary Value Analysis - Type of black box testing to test the boundaries between partitions instead of testing multiple values in the equivalence region.
 **Ex:** To test the age can be from 20 to 50 so test cases can be written for 19, 20 , 49, 50 , 51  
  
2. Equivalent Class Partitioning  - Test case design method that divides the input domain data into various equivalence data classes, assuming that data in each group behaves the same.  
**Ex.** Name should be within 5-20 text-only  
a. Test cases can be enter value 5-20 valid  
b. Enter less than 5 , Error should be the”Name must be between 5-20”  
c. Enter more than 20,  Error should be the”Name must be between 5-20”  
d. Leave blank or no text characters, invalid name  
  
3. Decision Table  - Technique based on cause-effect table used to test system behaviour in which the output depends on a large combination of input.  
 **Ex.** Navigate a user to the homepage if all blanks/specific blanks in the login section are filled in  
First and foremost, we need to identify the functionalities where the output responds to different input combinations, for each function divide the input set into possible smaller subsets that correspond to various outputs.  
  
For every function we create a decision table. The table consists of 3 main parts:  
  
a. List of all possible input combinations  
b. List of corresponding system behaviour  
c. T and F stands for correctness of input conditions  
  
4. Error Guessing  - Based on experiences of the test analysts. He/she will try to guess and assume the possible errors or error-prone situations which can prevail in the code; hence the test designers must be skilled and experienced testers.  
  
5. Change Request ( CR ) - Product before moving to production, if client needs any change on any existing feature with minimal changes required from our system. Those changes are generally not charged. Generally any bug fixes  
  
6. Feature Request ( FR ) - Before moving or after moving the product to prod the client has request for a feature which was not part of initial requirement and require efforts.

## Functional Testing  
      
**Overview:** Verifies that the software functions as intended, ensuring it meets the specified requirements and user expectations.  

**Example:**

-   **Scenario:** Testing an e-commerce website
-   **Test Case:** Verify that a user can successfully add items to the cart, proceed to checkout, and complete the purchase.

## Non-Functional Testing  
      
**Overview:** Evaluates aspects of the software that are not directly related to its functionality, such as performance, usability, security, and compatibility.  
      
**Examples:**

-   **Performance testing:** Measure response times, throughput, and resource utilization under various load conditions.
-   **Usability testing:** Evaluate the ease of use and user experience of the software.
-   **Security testing:** Identify vulnerabilities and potential security threats.
-   **Compatibility testing:** Verify that the software works as expected on different browsers, operating systems, and devices.

## Unit Testing  
      
**Overview:**  Tests individual components or units of code in isolation.  
      
**Example:**

-   **Scenario:** Testing a function that calculates the factorial of a number
-   **Test Case:** Create unit tests to verify that the function returns the correct factorial values for different inputs.

## Integration Testing  
      
**Overview:**  Tests how different components or modules of the software interact with each other.  
      
**Example:**

-   **Scenario:** Testing a web application
-   **Test Case:** Verify that the login functionality works correctly when integrated with the user database and authentication system.

## System Testing  
      
**Overview:**  Tests the entire system as a whole, ensuring it meets the specified requirements and functions as intended.  
      
**Example:**

-   **Scenario:** Testing a mobile app
-   **Test Case:** Verify that the app can be installed, launched, and used on different devices and operating systems.

## Regression Testing  
      
**Overview:** Retests previously tested functionalities to ensure that new changes have not introduced any defects.  
      
**Example:**

-   **Scenario:** Implementing a new feature in a web application
-   **Test Case:** Re-run existing test cases to verify that the new feature does not affect the functionality of existing features.

## Smoke Testing  
      
**Overview**: A quick and superficial test to verify that the critical functionalities of the software are working as expected.  
 
 **Example:**

-   **Scenario:** Deploying a new build of a web application
-   **Test Case:** Verify that the login page loads, users can log in successfully, and the main navigation menu is functional.

## Acceptance Testing  
      
**Overview:** Tests the software from the end-user's perspective to ensure it meets their requirements and expectations.  
      
**Example:**

-   **Scenario:** Launching a new e-commerce website
-   **Test Case:** Have potential customers evaluate the website's usability, design, and functionality to ensure it meets their needs.

## JMeter

It is a popular open-source performance testing tool that can be used to simulate load and measure the performance of web applications, APIs, and other systems. Here's a basic guide on how to use JMeter for performance testing.  
      
**Create a Test Plan**

-   Right-click on "Test Plan" in the tree view and select "Add" -> "Thread Groups" -> "Thread Group".  
    
-   Configure the number of threads (users), ramp-up period, loop count, and other thread group properties.  
      
**Add Samplers** 

-   Right-click on the Thread Group and select "Add" -> "Sampler".
-   Choose the appropriate sampler type based on your target:

-   **HTTP Request:** For web applications
-   **FTP Request:** For FTP servers
-   **JDBC Request:** For databases
-   **TCP Sampler:** For TCP-based protocols

-   Configure the sampler with the necessary parameters, such as URL, method, request data, etc.  
      
**Add Listeners**

-   Right-click on the Thread Group and select "Add" -> "Listener".
-   Choose the desired listener to view test results:

-   **View Results Tree:** Displays detailed information about each request.
-   **Graph Results:** Visualises response times, throughput, and other metrics.
-   **Summary Report:** Provides a summary of the test results.
-   **Aggregate Report:** Aggregates test results for multiple samplers.  
      
    

**Example Test Plan: Testing a Web Application** 

1.  Create a Thread Group with 50 threads, a ramp-up period of 60 seconds, and infinite loops.
2.  Add an HTTP Request sampler with the URL of your web application.
3.  Add a View Results Tree listener to view detailed request and response information.
4.  Run the test and analyse the results.  
      
**Additional Tips:**  

-   **Configure Assertions:** Use assertions to validate responses and identify errors.
-   **Use CSV Data Set Config:** To parameterize requests with different data sets.
-   **Implement Correlation:** Handle dynamic values in responses.
-   **Monitor System Resources:** Use JMeter's plugins to monitor server performance during the test.

## Quality assurance and Quality control  
      
**Quality Assurance:**

-   It ensures the prevention of defects in the process used to make software applications.
-   It involves process-oriented activities.
-   Aim to prevent defects.  
      
**Quality Control:** 
-   It executes the program or code to identify the defects in the software application.
-   It involves product-oriented activities.
-   Aim to identify and improve.

## STLC  
The software testing life cycle refers to all the activities performed during the testing of a software product. The phases include –  

-   **Requirement analyses and validation**: In this phase, the requirements documents are analyzed and validated, and the scope of testing is defined.
-   **Test planning**: In this phase, the test plan strategy is defined, the estimation of test effort is defined along with the automation strategy, and tool selection is done.
-   **Test Design and Analysis:** In this phase, test cases are designed, test data is prepared, and automation scripts are implemented.
-   **Test environment setup**: A test environment closely simulating the real-world environment is prepared.
-   **Test execution**: The test cases are prepared, and the bugs are reported and retested once resolved.
-   **Test closure and reporting**: A test closure report is prepared with the final test results summary, learning, and test metrics

## Dynamic vs Static Testing  
  
**Dynamic Testing**  
  
It involves in the execution of code and validates the output with the expected outcome.  
  
**Static Testing**  
  
It involves in reviewing the documents to identify the defects in the early stages of SDLC.

## Defect Life Cycle or Bug Life Cycle 

It is the specific set of states that a Bug goes through from discovery to defect fixation.  
      
**Bug Life Cycle phases/status:-** The number of states that a defect goes through varies from project to project. Below lifecycle diagram, covers all possible states  
      
    

-   **New:** When a new defect is logged and posted for the first time. It is assigned a status as NEW.
-   **Assigned:** Once the bug is posted by the tester, the lead of the tester approves the bug and assigns the bug to the developer team.
-   **Open**: The developer starts analysing and works on the defect fix.
-   **Fixed**: When a developer makes a necessary code change and verifies the change, he or she can make the bug status “Fixed.”
-   **Pending retest**: after fixing the defect the developer gives a particular code for retesting the code to the tester. Here the testing is pending on the tester’s end, the status assigned is “pending request.”
-   **Retest**: Tester does the retesting of the code, to check whether the defect is fixed by the developer or not and changes the status to “Re-test.”
-   **Verified**: The tester re-tests the bug after it got fixed by the developer. If there is no bug detected in the software, then the bug is fixed and the status assigned is “verified.”
-   **Reopen**: If the bug persists even after the developer has fixed the bug, the tester changes the status to “reopened”. Once again the bug goes through the life cycle.
-   **Closed**: If the bug no longer exists then the tester assigns the status “Closed.”
-   **Duplicate**: If the defect is repeated twice or the defect corresponds to the same concept of the bug, the status is changed to “duplicate.”
-   **Rejected**: If the developer feels the defect is not a genuine defect then it changes the defect to “rejected.”
-   **Deferred**: If the present bug is not of a prime priority and if it is expected to get fixed in the next release, then the status “Deferred” is assigned to such bugs
-   **Not a bug**: If it does not affect the functionality of the application then the status assign to a bug is “Not a bug”.
-   **New** – A bug or defect when detected is in a New state
-   **Assigned** – The newly detected bug when assigned to the corresponding developer is in the Assigned state
-   **Open** – When the developer works on the bug, the bug lies in the Open state
-   **Rejected/Not a bug** – A bug lies in rejected state in case the developer feels the bug is not genuine
-   **Deferred** – A deferred bug is one, fix which is deferred for some time(for the next releases) based on the urgency and criticality of the bug
-   **Fixed** – When a bug is resolved by the developer it is marked as fixed
-   **Test** – When fixed the bug is assigned to the tester and during this time the bug is marked as in Test
-   **Reopened** – If the tester is not satisfied with the issue resolution the bug is moved to the Reopened state
-   **Verified** – After the Test phase if the tester feels the bug is resolved, it is marked as verified
-   **Closed** – After the bug is verified, it is moved to Closed status.

## Functional Testing  

Focuses on verifying the software against functional requirements.  

-   **Unit Testing**: Tests individual components or functions of the software.
-   **Integration Testing**: Verifies the interactions between integrated components.
-   **System Testing**: Examines the complete system as a whole.
-   **User Acceptance Testing (UAT)**: Ensures the software meets business requirements and is user-friendly.
-   **Sanity Testing**: Confirms that minor changes or fixes have been implemented correctly.
-   **Smoke Testing**: Quickly checks if the critical functionalities are working after a build.

## Non-Functional Testing  


Focuses on attributes like performance, usability, and reliability.  

-   **Performance Testing**: Measures the responsiveness and stability under load.

-   **Load Testing**: Tests behavior under expected load.
-   **Stress Testing**: Examines limits by applying high levels of stress.
-   **Spike Testing**: Tests system behavior under sudden load spikes.

-   **Usability Testing**: Checks if the system is user-friendly.
-   **Compatibility Testing**: Ensures the software works across different devices, browsers, or environments.
-   **Security Testing**: Identifies vulnerabilities and ensures data protection.
-   **Scalability Testing**: Tests the system’s ability to handle growth.
-   **Reliability Testing**: Ensures consistent performance over time.

## Maintenance Testing  

Conducted after deployment to ensure continued performance.  

-   **Regression Testing**: Ensures new changes don’t break existing functionality.
-   **Retesting**: Verifies that fixed issues have been resolved.

## Specialized Testing  

For specific contexts or requirements.  

-   **Alpha Testing**: Done by internal teams before beta release.
-   **Beta Testing**: Performed by external users to provide feedback before launch.
-   **Accessibility Testing**: Ensures compliance with accessibility standards for users with disabilities.
-   **Mobile Testing**: Focused on mobile-specific issues like gestures, screen sizes, and battery usage.
-   **Big Data Testing**: Validates the processing of large volumes of data.
-   **IoT Testing**: Tests the functionality and security of IoT devices.

## Automated and Manual Testing  

-   **Manual Testing**: Performed by testers manually without automation.
-   **Automated Testing**: Uses tools to execute test scripts, e.g., Selenium, JUnit.

  

## Exploratory and Ad-hoc Testing  

-   **Exploratory Testing**: Involves testers exploring the system without predefined scripts.
-   **Ad-hoc Testing**: Performed without any structured test cases or plans.

## Other Types of Testing  

-   **Black-Box Testing**: Tester doesn’t know internal workings; focuses on inputs and outputs.
-   **White-Box Testing**: Tests internal structures or workings of an application.
-   **Grey-Box Testing**: Combines black-box and white-box testing techniques.
-   **End-to-End Testing**: Validates the complete workflow from start to finish.
-   **Localization Testing**: Ensures the software is adapted for a specific region or language.
-   **Recovery Testing**: Verifies the system’s ability to recover after failures.

## DDO

Defination of Done
