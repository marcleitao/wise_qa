# Software Quality

The first step to ensure quality while working in an Agile environment is to define a proper Definition of Done.
Must be defined by the team and acts as a checklist to guarantee a story was properly implemented. In terms of QA, should include a few stages to check the build's quality.

For each sprint the QA Engineer should help the developers to refine the story in order to entirely understand the use case. An unexpected behaviour of the system is a missing user story. While the code is being develop, the QA Engineer must be defining the automated tests to be delivered during that sprint and when the code is delivered, just wrap up the test code, test it and publish it in to the version control system. At that point, exploratory tests are executed and for each bug found, an automated test needs to be implemented. By the end of the sprint all those tests must be merged in to the existing automated test suite.

## Test Phases:
1. Unit Testing:
Written by developers are the fastest way to test, they are never too much.

2. API Mock Testing:
Written by developers but can also be developed by QA Engineers, will easily assert if an expected api call will be handled the proper way.

3. API Testing (Integration):
Written by QA Engineers, will check the proper integration between two systems

4. E2E Testing (Regression):
Written by QA Engineers, will check if the system as a whole behaves as expected.

5. Code Static Testing:
Using an external platform/tool, the code will be checked and make sure developers follow coding standards and best practices to avoid potential errors.

6. Security Testing:
Using an external platform/tool, checks the code for code vulnerabilities.

7. Exploratoring Testing:
Executed manually by QA Engineers, are used to identify flaws by trying to break the application. It does not follow any kind of test case.

8. Performance Testing:
Executed to ensure a build does not degradates the performance of the platform.

9. Acceptance Testing:
Executed in QA environment as a final signoff for the software quality, users stories need to be checked manually by QA Engineers and stakeholders to make sure the feature is ready to live.

Once a build passes all stages, we can have a certain confidence about the build quality and it's ready for live.

## Continuous Integration:
To speed up the quality process, the stages 1-6 must be included in a CI process so tests need to be automated.

## Test Management:
To manage all tests, a test management tool can be used but after a certain amount of tests it starts to become difficult to manage them. The best approach is to have stories with steps properly automated and it's easier to replace a story and replace an automated step than replace a bunch of tests.

## Automated Tests:
For each feature, automated tests should be created during the first week of the sprint to allow them to be used and properly tested during the second week. Tests to a feature should be finished by the end of the sprint.

## Environments:
Dev can be used for exploratory testing, QA environment to allow acceptance testing and live to be live (so no QA here!).
A proper virtual dev environment is crucial to implement a CI process. For it, it's required to maintain a snapshot of the live environment where the build is deployed, tested and destroyed when the stages finish successfully or not.

## Defect management:
When an issue is found, a bug needs to be recorded in the defect management tool and an automated test needs to be created to test that scenario in the future.

## Reporting:
Almost all test framework provides a report with the executed tests and for that we just need to export the results in to a dashboard and constantly provide updates.
