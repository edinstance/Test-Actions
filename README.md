# Test-Actions

This repository serves as a testing ground for GitHub actions that I am developing and planning to use in my projects.

## Actions Developed So Far:

1. **Create Branch for New Issue:**
   - This action automatically creates a branch for a new issue when a certain label is added to it.
   - Once the branch is created, it adds a comment to the issue with a link to the newly created branch.
  
2. **Run prettier and lint for a next project:**
   - This action runs on pull request
   - This action sets up node
   - It then installs all of the needed dependencies
   - It runs the lint commnand

3. **Run a python script:**
   - This action runs on request
   - It upgrades the version of pip being used
   - Then it installs all of the dependencies from a requirements.txt file
   - After that a step to run the script or run tests is needed but this has been left blank so it is more reuseable

4. **Deploy a postgres database to supabase:**
   - This action runs on request
   - It is based off of this [database example](https://github.com/edinstance/online-shop-database-example)
   - It tests if the configuration is valid before deploying
   - It does this by running against a docker postgres database
   - If liqiubase runs correctly then the supabase database is updated
   - Some GitHub secrets need to be configured for this but this is explained in the releveant [README.md](.github/workflows/postgres/README.md)

5. **Run cypress tests against a next.js project**
   - This action runs on pull request and workflow dispatch
   - This action sets up node
   - It then builds a docker image for the next.js project
   - Then it runs all of the docker images in detached mode
   - Finally it uses the Cypress action to run the tests
   
6. **Java Unit Tests**
   - This action runs on pull request and workflow dispatch
   - This action sets up JDK
   - Then runs the tests using maven
   - Finally it saves the tests results as an artifact

7. **Java Intergration Tests**
   - This action runs on pull request and workflow dispatch
   - This action uses github secrets to contain to contain the database enviroment variables
   - This action sets up JDK
   - It then builds a docker image for the Java project
   - Then it runs all of the docker images in detached mode
   - Then it installs the correct dependencies and runs tests using maven
   - Finally it saves the test results as an artifact 
   
Feel free to explore the actions further and contribute to their development!
