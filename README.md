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

# CodeCommit
- **Version Control** is the ability to understand the various changes that happened to the code over time (and possible roll back).
- All these are enabled by using a version control system such as Git
- A Git repository can live on one's machine, but it usually lives on a central online repository
- Benefits are:
   - Collaborate with other develops
   - Make sure the code is backed-up somewhere
   - Make sure it's fully viewable and auditable
- Git repositories can be expensive.
- The industry icludes:
   - GitHub: free public repositories, paid private ones
   - BitBucket
   - Etc...
- And AWS CodeCommit:
   - private Git repositories
   - No size limit on repositories (scale seamlessly)
   - Fully managed, highly available
   - Code only in AWS Cloud account => increased security and compliance
   - Secure (encrypted, access control, etc...)
   - Integrated with Jenkins / CodeBuild / other CI tools
 
# CodeBuild
- Fully managed build service
- Alternative to other build tools such as Jenkins
- Continuous scaling (no servers to managed or provision - no build queue)
- Pay for usage: the time it takes to complete the builds
- Leverages Docker under the hood for reproducible builds
- Possibility to extend capabilities leveraging our own base Docker images
- Secure: Integration with KMS for encryption of build artifacts, IAM for build permissions, and VPC for network security, CloudTrail for API calls logging
- Source Code from GitHub / CodeCommit / CodePipeline / S3...
- Build instructions can be define in code (buildspec.yml file)
- Output logs to Amazon S3 & AWS CloudWatch Logs
- Metrics to monitor CodeBuild statisitcs
- Use CloudWatch Events to detect failed builds and trigger notifications
- Use CloudWatch Alarms to notify if you need "thresholds" for failures
- CloudWatch Events / AWS Lambda as a Glue
- SNS notifications
### sample of buildspec.yml file
```
version: 0.2

phases:
build:
  commands:
    - echo Building...
artifacts:
  files:
    - '**/*'
  secondary-artifacts:
    artifact1:
      files:
        - directory/file1
      name: secondary-artifact-name-1
    artifact2:
      files:
        - directory/file2
      name: secondary-artifact-name-2
```      

# CodeDeploy
- We want to deploy our application automatically to many EC2 instances
- There are several ways to handle deployments using open source tools (Ansible, Terraform, Chef, Puppet, etc...)
- We can use the managed Service AWS CodeDeploy
- EC2 instances are grouped by deployment group (dev/test/prod)
- Lots of flexibility to define any kind of deployments
- CodeDeploy can be chained into CodePipeline and use artifacts from there
- Note: Blue / Green only works with EC2 instances (not on premise)
- Support for AWS Lambda deployments, EC2
- CodeDeploy does not provision resources

### AWS CodeDeploy - Steps to make it work
- Each EC2 Machine (or On Premise machine) must be running the CodeDeploy Agent
- The agent is continuously polling AWS CodeDeploy for work to do
- CodeDeploy sends **appspec.yml** file.
- Application is pulled from GitHub or S3
- EC2 will run the deployment instructions
- CodeDeploy Agent will report of success / failure of deployment on the instance
### sample of appspec.yml file
```
version: 0.0
os: linux
files:
   - source: /index.html
      destination: /var/www/html
hooks:
   ApplicationStop:
      - location: scripts/stop_server.sh
        timeout: 300
        runas: root
        
   AfterInstall:
      - location: scripts/after_install.sh
        timeout: 300
        runas: root
        
   BeforeInstall:
      - location: scripts/install_dependencies.sh
        timeout: 300
        runas: root
        
   ApplicationStart:
      - location: scripts/start_server.sh
        timeout: 300
        runas: root
        
   ValidateService:
      - location: scripts/validate_service.sh
        timeout: 300
```        
