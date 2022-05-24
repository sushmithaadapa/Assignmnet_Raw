RawInnovation - Evernote UI App 
This repository contains a selenium-cucumber-java project with project Page Objects,PageFactory are used and libraries that demostrate testing the Evernote login & Create functionality using Cucumber BDD framework using java as the programming language.

Pre-Requisites
JDK
Maven
Eclipse
Eclipse plugin for
Junit
Cucumber

Develop automation scripts using BDD approach - Cucumber with Java
Tests are written in the cucumber framework using Gherkin keywords.

Dependencies to add in the pom.xml file
   - Cucumber-junit
   - Junit
   - Cucumber-java
   - Selenium-java
   - webdrivermanager
   - rest-assured
 
Stepdefinition folder - Inside the stepdefinition folder the main class and the test runner class is created.
Feature file - Feature files to run the script
DriverScripts - Generic Libraries for WebDriver actions.

Tests Covered :

 1) Unsuccessful login functionality for the page https://www.evernote.com/Login.action with Invalid email.
 2) Successful login functionality for the page https://www.evernote.com/Login.action with Valid email.
 3) Create a note under Notes Header followed by the logout.
 4) Login again and verify the created note is present or not in step 3.

To build the communication between Feauture file and Stepdefinition file, Test runner class is created.
  Options to add in a Testrunner class
       1) To run the cucumber @Runwith(cucumber.class) is usesd
       2) Then to build the communication @cucumberOptions(features="./src/test/resources/Features",glue={"StepDefinitions"} is used.
       3) To display the output in color format monochrome=true is used
       4) To generate reports
          * To generate the report in xml format plugin= {"pretty", "junit:target/JUNITReports/report.xml"} is used
          * To generate the report in html format plugin= {"pretty", "html:target/HTMLReports/report.html"} is used
          * To generate the report in json format plugin= {"pretty", "json:target/JSONReports/report.json"} is used
It generates Junit reports in xml format.
