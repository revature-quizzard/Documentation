# Workflows


## Git Branching/Workflow
 -	Main
    -	dev (extensive testing here)
        - pre-dev (integration testing here)
           -	feature-something (unit testing here)
              - user-story-developer (Develop your units tests)
              -	user-story-developer (Develop your units tests)
           - feature-something-else (unit testing here)
              -	user-story-developer (Develop your units tests)
              -	user-story-developer (Develop your units tests)
    - pipeline

Merge only up one layer. Review code and check unit test coverage. Git flow managers should have final say over pushes to into pre-dev and above. Utilize the review functionality for merges.

## Bugs/Issue Tracking
Create a github issue. Make sure to include explanation of how the bug was encountered, and what problems it caused. What did you expect to happen? What did happen instead?
Git flow team will review bugs and get them to the appropriate parties.

## Documenting Java
Use java doc comments /** and include all @params, @return, @throws, and @author with descriptions. Write verbose comments explaining the use of classes, and public methods. Include private methods if they need any explanation to others.
Generate a set of javadocs which use these annotations. IntelliJ > Code > Generate Java Docs.

## Documenting JS
Use inline comments, be descriptive. No generation of Javadoc similar documentation. We should make sure to include author, parameters, and return results.

