# CICD Overview

### Continuous Integration
- Developers push the code to a code repository often (GitHub/ CodeCommit / Bitbucket / etc...)
- A testing / build server checks the code as soon as it's pushed (CodeBuild / Jenkins CI / etc...)
- The developer gets feedback about the tests and checks that have passed / failed
- Find bugs early, fix bugs
- Deliver faster as the code is tested
- Deploy often
- Happier developers, as they're unblocked

### Continuous Delivery
- Ensure that the software can be released reliably whenever needed
- Ensures deployments happen often and are quick
- Shift away from "one release every 3 months" to "5 releases a day"
- That usally means automated deployment
   - Code Deploy
   - Jenkins CD
   - Spinnaker
   - Etc...

### Continuous Delivery vs Continuous Deployment
- Continuous Deplivery
   - Ability to deploy often using automation
   - May involve a manual step to "approve" a deployment
   - The deployment itself is still automated and repeated!
- Continuous Deployment
   - Full automation, every code change is deployed all the way to production
   - No manual intervention of approvals

# Technology Stack for CICD
<img src="https://user-images.githubusercontent.com/86287920/185820779-e7e8553a-e8a3-4ddd-a8e6-bbffcfeae22a.PNG">

### Reference Links for Domain 1
I use the documentation a lot in this course. Here are all the links that are visited during this section. I recommended you read through them in your own time, as I judge them to have some importance for your understanding of the services and the exam. Happy reading!
#### CodeCommit
- https://www.atlassian.com/git/tutorials/using-branches
- https://docs.aws.amazon.com/codecommit/latest/userguide/auth-and-access-control-iam-identity-based-access-control.html
- https://aws.amazon.com/blogs/devops/refining-access-to-branches-in-aws-codecommit/
- https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-notify.html
- https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-repository-email.html
- https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-notify-lambda.html
- https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-migrate-repository-existing.html
#### CodeBuild
- https://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html
- https://docs.aws.amazon.com/codebuild/latest/userguide/samples.html
- https://docs.aws.amazon.com/codebuild/latest/userguide/sample-docker.html
- https://aws.amazon.com/blogs/devops/validating-aws-codecommit-pull-requests-with-aws-codebuild-and-aws-lambda/
#### CodeDeploy
- https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_MinimumHealthyHosts.html
- https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html
- https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html#appspec-hooks-server
- https://docs.amazonaws.cn/en_us/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html#reference-appspec-file-structure-environment-variable-availability
- https://docs.aws.amazon.com/codedeploy/latest/userguide/monitoring-cloudwatch-events.html
- https://aws.amazon.com/blogs/devops/view-aws-codedeploy-logs-in-amazon-cloudwatch-console/
- https://docs.aws.amazon.com/codedeploy/latest/userguide/monitoring-sns-event-notifications.html
- https://docs.aws.amazon.com/codedeploy/latest/userguide/deployments-rollback-and-redeploy.html
- https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-groups-configure-advanced-options.html
- https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-on-premises.html
- https://docs.aws.amazon.com/codedeploy/latest/userguide/register-on-premises-instance-iam-user-arn.html
- https://docs.aws.amazon.com/codedeploy/latest/userguide/register-on-premises-instance-iam-session-arn.html
- https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-configurations.html#deployment-configuration-lambda
- https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html#appspec-hooks-lambda
#### CodePipeline
- https://docs.aws.amazon.com/codepipeline/latest/userguide/reference-pipeline-structure.html#action-requirements
- https://docs.aws.amazon.com/codepipeline/latest/userguide/best-practices.html#use-cases
- https://docs.aws.amazon.com/codepipeline/latest/userguide/actions-invoke-lambda-function.html
- https://docs.aws.amazon.com/codepipeline/latest/userguide/actions-create-custom-action.html
- https://docs.aws.amazon.com/codepipeline/latest/APIReference/API_PutJobSuccessResult.html
- https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/continuous-delivery-codepipeline.html
- https://docs.aws.amazon.com/codepipeline/latest/userguide/tutorials-cloudformation.html
- https://github.com/aws-samples/codepipeline-nested-cfn
- https://aws.amazon.com/blogs/devops/implementing-gitflow-using-aws-codepipeline-aws-codecommit-aws-codebuild-and-aws-codedeploy/
#### CodeStar
- https://docs.aws.amazon.com/codestar/latest/userguide/templates.html
#### Jenkins
- https://aws.amazon.com/getting-started/projects/setup-jenkins-build-server/
- https://wiki.jenkins.io/display/JENKINS/Amazon+EC2+Plugin
- https://aws.amazon.com/blogs/devops/setting-up-a-ci-cd-pipeline-by-integrating-jenkins-with-aws-codebuild-and-aws-codedeploy/
- https://wiki.jenkins.io/display/JENKINS/AWS+CodeBuild+Plugin
- https://wiki.jenkins.io/display/JENKINS/Amazon+EC2+Container+Service+Plugin
- https://wiki.jenkins.io/display/JENKINS/Artifact+Manager+S3+Plugin
- https://wiki.jenkins.io/display/JENKINS/AWS+CodePipeline+Plugin
