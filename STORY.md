# The Story

## Application Tests

Authentication and authorization are critical parts of access to all of WhizCorps' services. It is implemented as a central service that other applications use through OIDC and OAUTH2.
Users are redirected to the authentication service for log-in and application-role selection when they access any other service. Should the authentication service be down, no other service will be accessible to users.
In the last months, this has caused multiple problems because the authentication service became inaccessible after the deployment of a new version. Corporate has decided that these issues can no longer be allowed to happen and has tasked you, Alice, and Bob with the creation of application and integration tests for the authentication service.

You are to evaluate the feasibility of using different test automation frameworks/tools for tests against the authentication service's GUI, API, and OIDC/OAUTH2 capabilities. Additionally, you are to propose how these new tests are to be integrated into the build and deployment pipelines of the authentication service.

## Task

* Brainstorm all the problems and complexity
* Find ways to test your application during the build and/or deployment process
* Find ways to test the state your application after deployment
* How could you use these tests automatically rollback your application in case of problems?
  * How do we have to handle feedback of tests?
  * Do we have to use specific deployment strategies?
  * Does the application have to follow any design principles for this?
  * Does the application-infrastructure have to follow any design principles for this?
* Prepare for a discussion round with your colleagues Alice and Bob


## Questions to get started

* Should you use the same framework for GUI, API and OIDC tests?
* Should you focues on one aspect of the service over another (GUI > OIDC >> API, GUI = OIDC >> API, ... )?
* Are there any problems if you use "automation tools" instead of frameworks?
* Are there any possible problems if you use framework that should be kept in mind?
* How can you integrate this into a build or deployment pipeline?
* At which step of the pipeline would you integrate these tests (multiple?)?