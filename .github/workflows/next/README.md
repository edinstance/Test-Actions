# Next.js

The lint example runs the lint command in a next.js application. I normally setup this command to lint the code using eslint and also check if the formatting is correct using prettier.

The cypress example was created for an internal project at one of my previous companies, It was used for a next.js project that uses [cypress.io](https://www.cypress.io/) to run both end to end and component tests. The project required a backend to run against which is why the env needs a url from Github secrets. The project is run using docker, and was composed of the next.js image and a wiremock image to act as a mock backend for tests. Finally it uses the Cypress action to run the tests.