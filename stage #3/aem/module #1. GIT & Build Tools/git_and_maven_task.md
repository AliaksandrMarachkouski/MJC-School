## Git & Build tools

### Timeline
The recommended timeline for the whole module is 1 week.

### Git
To cover this topic please refer to the Git task of MJC-School first module (master branch)

[module #1. GIT & Build Tools](https://github.com/mjc-school/MJC-School/tree/master/stage%20%233/java/module%20%231.%20GIT%20%26%20Build%20Tools)

Links: 
- [Understanding Git — Data Model](https://medium.com/hackernoon/https-medium-com-zspajich-understanding-git-data-model-95eb16cc99f5)
- [Understanding Git — Branching](https://medium.com/hackernoon/understanding-git-branching-2662f5882f9)
- [Understanding Git — Index](https://medium.com/hackernoon/understanding-git-index-4821a0765cf)
- [GitHub flow (Optional)](https://docs.github.com/en/get-started/quickstart/github-flow)
- [Git flow (Optional)](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [Trunk Based development (Optional)](https://www.toptal.com/software/trunk-based-development-git-flow)

### Maven
Topics: 
- What are build tools? Why are they used?
- What can Maven manage?
- What is a Maven Repository? What types are there?
- What are Maven dependencies?
- Name Maven scopes and their definitions.
- Describe Maven lifecycles, phases, goals, tasks.
- What are Maven Plugins?
- What is pom.xml structure?
- Be familiar with parents/multimodule projects.

Links
- [Maven Getting Started Guide](https://maven.apache.org/guides/getting-started/index.html)
- [Maven Tutorial](https://www.tutorialspoint.com/maven/maven_overview.htm)


#### Task
1. Install Maven
2. Assemble custom jar `utils-1.3.5.jar`.
    It should be compatible with java 8. 
    The manifest file should contain the name and version of your jar.
    The jar should contain class `StringUtils` with method `boolean isPositiveNumber(String str)`.
    Use `Apache Commons Lang 3.10` library to implement this method.
    Write one any unit test for your `StringUtils.isPositiveNumber(String str)` using `JUnit 4.12`.
3. Create a project `multi-project` with two subprojects `core` and `api`.
    The `core` subproject should contain class `Utils` with method `boolean isAllPositiveNumbers(String... str)`.
    Use `utils-1.3.5.jar` from the previous task to implement this method.
    The `api` subproject should contain class `App` with the `main` method.
    Call `Utils.isAllPositiveNumbers("12", "79")` from the `main` method of `api` subproject.
