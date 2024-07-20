# Automation of capacity control service

A workflow for one of our capacity control systems was implemented as
a disjoint set of AWS components some of which were created and configured
manually using AWS console. On-call engineers had to manually run and verify
the execution results of these components. This process resulted in poor 
operability, documentation bloated with dozens of manual steps, and a high 
rate of human errors. Additionally, deploying the workflow to new environments
was challenging.

My task was to join all the workflow parts, automate execution kick-off,
improve errors handling, results validation and preparation of the final
report for an on-call engineer.

I used AWS StepFunction to join all the workflow components and to control
its execution. Additional workflow steps were introduced to replace manual 
tasks, automatically validate results, and prepare data in an easy-to-use format.
Deployment and configuration of all the components were covered by AWS CDK
(Infrastructure as a code) scripts.

As a result of this automation integration, we significantly reduced 
the on-call burden by eliminating most manual steps and improved overall system 
stability by minimizing human errors. With IaC approach we were able to
maintain consistency of our test and production environments.
