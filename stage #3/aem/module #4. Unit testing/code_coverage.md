## Code Coverage

Code coverage means measuring how much of your code is executed during your unit tests. 
Basically, that means that after running your unit tests, you get a report showing you how many percent of the code that was executed during the tests, 
and also what lines precisely that were executed.

With the code coverage report in hand, you can analyse what parts of your code that was not run, and modify your unit tests so these parts of the code are executed.

The larger the coverage, the closer to 100%, that is, the better chances you have of having bug free code. 
Having a 100% code coverage though, is not a guarantee that your code is bug free. 
For instance, code coverage does not guard against bugs that are caused by incorrect implementations of the requirements. 
The code may work just fine, but if it's not what the client asked for, it's still a bug.

To measure code coverage you need a coverage tool. Here is a small, but probably not exhaustive, list of code coverage tools for Java:

1. IntelliJ IDEA Coverage
2. Emma - http://emma.sourceforge.net/
3. EclEmma - http://www.eclemma.org/

IntelliJ IDEA has built-in code coverage from version 7.0. IntelliJ IDEA both has its own code coverage engine, and it can use Emma.

Emma is an open source code coverage tool for Java. You can run it as part of your Ant or Maven builds.

EclEmma is Emma in Eclipse.

I'll get into more detail with some of these coverage tools.

