## Local Environment Setup

JUnit is a framework for Java, so the very first requirement is to have JDK installed in your machine.

### Step 1: Verify Java Installation in Your Machine

First of all, open the console and execute a java command based on the operating system you are working on.

  Windows	Open Command Console	c:\> java -version
  
  Linux	Open Command Terminal	$ java -version
  
  Mac	Open Terminal	machine:~ joseph$ java -version


Let's verify the output for all the operating systems −

  Windows	
  java version "1.8.0_101"
  Java(TM) SE Runtime Environment (build 1.8.0_101)


  Linux	
  java version "1.8.0_101"
  Java(TM) SE Runtime Environment (build 1.8.0_101)

  Mac	
  java version "1.8.0_101"
  Java(TM) SE Runtime Environment (build 1.8.0_101)


### Step 2: Set JAVA Environment

Set the JAVA_HOME environment variable to point to the base directory location where Java is installed on your machine. For example.

  Windows	Set the environment variable JAVA_HOME to C:\Program Files\Java\jdk1.8.0_101
  
  Linux	export JAVA_HOME = /usr/local/java-current
  
  Mac	export JAVA_HOME = /Library/Java/Home


Append Java compiler location to the System Path.

  Windows	Append the string C:\Program Files\Java\jdk1.8.0_101\bin at the end of the system variable, Path.
  
  Linux	export PATH = $PATH:$JAVA_HOME/bin/
  
  Mac	not required
  

Verify Java installation using the command java -version as explained above.

### Step 3: Download JUnit Archive

Download the latest version of JUnit jar file from http://www.junit.org. 
At the time of writing this tutorial, we have downloaded Junit-4.12.jar and copied it into C:\>JUnit folder.

### Step 4: Set JUnit Environment

Set the JUNIT_HOME environment variable to point to the base directory location where JUNIT jar is stored on your machine. 
Let’s assuming we've stored junit4.12.jar in the JUNIT folder.

Windows
Set the environment variable JUNIT_HOME to C:\JUNIT

Linux
export JUNIT_HOME = /usr/local/JUNIT

Mac
export JUNIT_HOME = /Library/JUNIT


### Step 5: Set CLASSPATH Variable

Set the CLASSPATH environment variable to point to the JUNIT jar location.

Windows
Set the environment variable CLASSPATH to %CLASSPATH%;%JUNIT_HOME%\junit4.12.jar;.;

Linux
export CLASSPATH = $CLASSPATH:$JUNIT_HOME/junit4.12.jar:.

Mac
export CLASSPATH = $CLASSPATH:$JUNIT_HOME/junit4.12.jar:.


### Step 6: Test JUnit Setup

Create a java class file name TestJunit in C:\>JUNIT_WORKSPACE

    import org.junit.Test;
    import static org.junit.Assert.assertEquals;
    
    public class TestJunit {
      @Test
      public void testAdd() {
        String str = "Junit is working fine";
        assertEquals("Junit is working fine",str);
      }
    }

Create a java class file name TestRunner in C:\>JUNIT_WORKSPACE to execute test case(s).

    import org.junit.runner.Result;
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

### Step 7: Verify the Result

Compile the classes using javac compiler as follows −

C:\JUNIT_WORKSPACE>javac TestJunit.java TestRunner.java
Now run the Test Runner to see the result as follows −

C:\JUNIT_WORKSPACE>java TestRunner
Verify the output.

true
