# Highlights of contributions at Amazon since Jan 2022

I worked at Amazon Supply Chain Optimization Technologies (SCOT) in
Retail Capacity Control (RCC) team. As a team we were developing and 
maintaining several systems that helps Amazon’s Retail to distribute 
inbound inventory across Fulfillment centers (warehouses).

As an SDE I made the following contributions:

1. Designed and implemented automaton workflow for one of Capacity Control
services (FCC). The workflow was implemented using AWS serverless services such as
Lambda, Step Function, S3, DynamoDB, EventBridge. All components were
deployed using AWS CDK (IaC).

2. I created automated integration tests for FCC service to enable 
automated CI/CD pipeline. It significantly improved Time-to-production metric
for that service.

3. I was leading a project to expand the list of supported inventory types 
for one of our Capacity Control systems. My work included design documents
preparation, data analisys, communication with engineers from different teams,
end-to-end testing and production rollout.

4. I participated in development of next-gen Capacity Control system
that was implemented using AWS SimpleWorkflow service. I added support of
control operations to pause / resume or interrupt computation.

5. I designed and implemented a mechanism to automatically detect and
restart failed zombie-tasks in proprietarty distributed jobs scheduler.
