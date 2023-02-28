Second cucumber project -

This project uses BDD with Cucumber to ensure that the requirements are met and the application works as expected. The
Gherkin syntax consists of different parts such as: Features, Scenarios and Steps. The tests are written in the Gherkin syntax, which
is a plain-text language that is easy to read and write.

Feature: A feature describes the functionality of the system that the user wants to perform.
Scenario: A scenario represents a specific example of how the feature should behave in different situations.
Steps: Steps are the actions that need to be taken to test the scenario.

The folder structure is:
Pages: Where all web page elements and methods are stored.
Steps: Performs actions such as interacting with the web page, assertions and calling other methods using test scripts.
Utilities: The Utilities folder is a helper class or set of classes that provide reusable functions or services to
perform specific tasks.
Runners: Contains annotations and configuration options that specify how the BDD framework should run the tests.

To execute specific suites with tags using Maven commands, you need to add the surefire plugin to your pom.xml file,
With this plugin configuration, you specify the location of the TestNG XML file that contains the specific test suites
and tags you want to execute. You can add tags to your feature files to group them and execute only the specific
scenarios that match those tags. To execute the specific suites with tags, you can use the following Maven command:

mvn test -Dcucumber.options="--tags @Smoke"