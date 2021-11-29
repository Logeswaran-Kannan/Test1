### selenium-cucumber-java

This repository contains a collection of sample `selenium-cucumber-java` projects and libraries that demonstrate how to
use the tool and develop automation script using the Cucumber (v 3.0.0) BDD framework with Java as programming language.
It also generate `screen shots` for your tests if you enable it and also generate `error shots` for your failed test cases as well.

### Installation (pre-requisites)

1. JDK 1.8+ (make sure Java class path is set)
2. Maven (make sure .m2 class path is set)
3. Eclipse
4. Eclipse Plugins for
    - Maven
    - Cucumber
5. Browser driver (make sure you have your desired browser driver and class path is set)

### Framework set up

Fork / Clone repository from [here]( https://github.com/amiya-pattnaik/selenium-cucumber-java) or download zip and set
it up in your local workspace.

### Run Some Sample Tests

Open command prompt / power shell (for windows OS) and navigate to the project directory
type `mvn clean test` command to run features. With this command it will invoke the default Firefox browser and will
execute the tests.

Please note that browser drivers are not included as part of this framework. The reason for not including is that
selenium browser driver version are varies based on the browser version that you are using and also selenium server
version.


### Reporters

Once you ran your tests you can generate the various types of reports. This framework `selenium-cucumber-java` uses
several different types of test reporters to communicate pass/failure.


##### Extent Spark Reports

The Framework uses [Spark Reports Framework](http://www.extentreports.com/docs/versions/4/java/spark-reporter.html) to
generate the HTML Test Reports

The example below is a report generated by Extent Reports open-source library.

<img src="https://github.com/amiya-pattnaik/selenium-cucumber-java/blob/master/src/main/resources/demo/demo.png" height="400px" width="600"/>

### Develop automation scripts using BDD approach - Cucumber-Java

There are already many predefined StepDefinitions which is packaged under `/steps/Commonsteps.java` will help you speed
up your automation development that support both your favorite workaday helpers methods.

Tests are written in the Cucumber framework using the Gherkin Syntax. More about Gherkin & Cucumber can be found
at https://cucumber.io/docs/reference A typical test will look similar to this:

```
Feature: WishList Table

Scenario: Select wishlist Product
Given I add four different products to my wish list
When I view my wishlist table
Then I find total four selected item in my Wishlist
When I search for lowest price product
And I am able to add the lowest price item to my cart
Then I am to verify the item in my cart
