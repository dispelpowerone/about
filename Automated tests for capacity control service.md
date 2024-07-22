# Automated tests for capacity control service

One of our Capacity Control services had no integration end-to-end tests.
It was built using a combination of Java microservices and AWS components,
including StepFunctions, Lambdas. Also, the service had a bidirectional 
dependency on an external service, complicating the creation of tests.
Without tests engineers had to manually approve the service deployment after 
performing manual tests in the staging environment. On average, deployments 
took about 3 hours and required periodic interventions from engineers.
This process limited the team to 1-2 deployments per week, causing significant 
delays in pushing critical updates to production.

My task was to design and implement a set of end-to-end tests that could be 
executed automatically using CI/CD pipeline whenever there were updates to 
the codebase or dependencies.

I implemented a lightweight service that mimicked the interface of the real 
external dependency, allowing us to mock it in the test environment.
I created a set of classes to monitor and verify the execution of the Capacity 
Control service.
Finally, I developed a comprehensive suite of tests to cover various workflow
scenarios.

The deployment pipeline for the Capacity Control service was fully automated, 
eliminating the need for engineer intervention. The average time-to-production 
was reduced from several days to just dozens of minutes.
