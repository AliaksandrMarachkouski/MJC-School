## Testing Framework

JUnit is a Regression Testing Framework used by developers to implement unit testing in Java, and accelerate programming speed and increase the quality of code. 
JUnit Framework can be easily integrated with either of the following −

Eclipse

Ant

Maven

### Features of JUnit Test Framework

JUnit test framework provides the following important features −

Fixtures

Test suites

Test runners

JUnit classes


Fixtures

Fixtures is a fixed state of a set of objects used as a baseline for running tests. 
The purpose of a test fixture is to ensure that there is a well-known and fixed environment in which tests are run so that results are repeatable. 
It includes −

setUp() method, which runs before every test invocation.

tearDown() method, which runs after every test method.

Let's check one example −

    import junit.framework.*;

    public class JavaTest extends TestCase {
      protected int value1, value2;
   
      // assigning the values
      protected void setUp(){
        value1 = 3;
        value2 = 3;
      }

      // test method to add two values
      public void testAdd(){
        double result = value1 + value2;
        assertTrue(result == 6);
      }
    }

### Test Suites

A test suite bundles a few unit test cases and runs them together. 
In JUnit, both @RunWith and @Suite annotation are used to run the suite test. 
Given below is an example that uses TestJunit1 & TestJunit2 test classes.

    import org.junit.runner.RunWith;
    import org.junit.runners.Suite;

    //JUnit Suite Test
    @RunWith(Suite.class)

    @Suite.SuiteClasses({ 
      TestJunit1.class ,TestJunit2.class
    })

    public class JunitTestSuite {
    }
    
    import org.junit.Test;
    import org.junit.Ignore;
    import static org.junit.Assert.assertEquals;

    public class TestJunit1 {

      String message = "Robert";	
      MessageUtil messageUtil = new MessageUtil(message);
   
      @Test
      public void testPrintMessage() {	
          System.out.println("Inside testPrintMessage()");    
          assertEquals(message, messageUtil.printMessage());     
      }
    }
    
    import org.junit.Test;
    import org.junit.Ignore;
    import static org.junit.Assert.assertEquals;

    public class TestJunit2 {

      String message = "Robert";	
      MessageUtil messageUtil = new MessageUtil(message);
 
      @Test
      public void testSalutationMessage() {
          System.out.println("Inside testSalutationMessage()");
          message = "Hi!" + "Robert";
          assertEquals(message,messageUtil.salutationMessage());
      }
    }

### Test Runners

Test runner is used for executing the test cases. Here is an example that assumes the test class TestJunit already exists.

    import org.junit.runner.JUnitCore;
    import org.junit.runner.Result;
    import org.junit.runner.notification.Failure;

    public class TestRunner {
      public static void main(String[] args) {
          Result result = JUnitCore.runClasses(TestJunit.class);
		
          for (Failure failure : result.getFailures()) {
            System.out.println(failure.toString());
          }
		
          System.out.println(result.wasSuccessful());
      }
    }

### JUnit Classes

JUnit classes are important classes, used in writing and testing JUnits. Some of the important classes are −

Assert − Contains a set of assert methods.

TestCase − Contains a test case that defines the fixture to run multiple tests.

TestResult − Contains methods to collect the results of executing a test case.
