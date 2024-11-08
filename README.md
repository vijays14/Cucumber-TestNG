# Cucumber-TestNG
Integrating Cucumber-selenium-TestNG

TestNG - Cucumber Integration
Install Eclipse IDE
Install TestNG and Cucumber Plugins in the Eclipse IDE
Create a Maven project and use the default Arch type to create the following folders in the project
src/main/java
src/main/resources
src/test/java
src/test/resources
Under the src/test/resources folder create a new folder named Feature
Again under the Feature folder create a file login.feature. The .feature extension is for the cucumber
Given, When, Then, And - is the Gherkin syntax which helps non-technical ppl understand the automation script steps
Using the Gherkin syntax, write the steps at the login.feature file
Now run the login.feature file as the cucumber feature
It will throw error as the required Dependencies are missing - Open the POM file and add the following dependencies
Cucumber- Java 
Cucumber -TestNG
TestNG
Selenium-Java
These are the dependencies needed to run this test
We will get the boilerplate code template to write the Glue code for the Cucumber at the console
Using the Template write the selenium-java code to login to the page using credentials and enter into the application. Then finally close the application
Now run the code as a cucumber feature and see if all the tests have passed.
Now it is time to write the TestRunner class - and that will be executed using the TestNG
Under the src/test/java directory , create a new folder named TestRunner.Under which we need to create a class file named cucumberTestRunner
In the cucumberTestRunner, add the following annotation and the respective parameters
@CucumberOptions
(tags =””,
features={”src/test/resources”}, its the relative path where Features folder is located
glue={”stepDefinitions”}, its the folder where the actual selenium code is added
Plugin = {“pretty”, “html:target/testreportfilename.html”} its where the html report will be stored in the given name )

To parameterise the test data use the following steps in the login.feature file


Then update the stepdefinition java file accordingly as mentioned below


