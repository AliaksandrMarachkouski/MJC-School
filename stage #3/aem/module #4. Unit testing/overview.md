## Overview


Testing is the process of checking the functionality of an application to ensure it runs as per requirements. Unit testing comes into picture at the developers’ level; it is the testing of single entity (class or method). Unit testing plays a critical role in helping a software company deliver quality products to its customers.

Unit testing can be done in two ways − manual testing and automated testing.

### Manual Testing

Executing a test cases manually without any tool support is known as manual testing.

Time-consuming and tedious − Since test cases are executed by human resources, it is very slow and tedious.

Huge investment in human resources − As test cases need to be executed manually, more testers are required in manual testing.

Less reliable − Manual testing is less reliable, as it has to account for human errors.

Non-programmable − No programming can be done to write sophisticated tests to fetch hidden information.

### Automated Testing

Taking tool support and executing the test cases by using an automation tool is known as automation testing.

Fast − Automation runs test cases significantly faster than human resources.

Less investment in human resources − Test cases are executed using automation tools, so less number of testers are required in automation testing.

More reliable − Automation tests are precise and reliable.

Programmable − Testers can program sophisticated tests to bring out hidden information.

### What is JUnit ?

JUnit is a unit testing framework for Java programming language. It plays a crucial role test-driven development, and is a family of unit testing frameworks collectively known as xUnit.

JUnit promotes the idea of "first testing then coding", which emphasizes on setting up the test data for a piece of code that can be tested first and then implemented. This approach is like "test a little, code a little, test a little, code a little." It increases the productivity of the programmer and the stability of program code, which in turn reduces the stress on the programmer and the time spent on debugging.

### Features of JUnit

JUnit is an open source framework, which is used for writing and running tests.

Provides annotations to identify test methods.

Provides assertions for testing expected results.

Provides test runners for running tests.

JUnit tests allow you to write codes faster, which increases quality.

JUnit is elegantly simple. It is less complex and takes less time.

JUnit tests can be run automatically and they check their own results and provide immediate feedback. There's no need to manually comb through a report of test results.

JUnit tests can be organized into test suites containing test cases and even other test suites.

JUnit shows test progress in a bar that is green if the test is running smoothly, and it turns red when a test fails.

### What is a Unit Test Case ?

A Unit Test Case is a part of code, which ensures that another part of code (method) works as expected. To achieve the desired results quickly, a test framework is required. JUnit is a perfect unit test framework for Java programming language.

A formal written unit test case is characterized by a known input and an expected output, which is worked out before the test is executed. The known input should test a precondition and the expected output should test a post-condition.

There must be at least two unit test cases for each requirement − one positive test and one negative test. If a requirement has sub-requirements, each sub-requirement must have at least two test cases as positive and negative.
