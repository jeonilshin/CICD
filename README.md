# CICD Overview
### Continuous Integration
- Developers push the code to a code repository often (GitHub/ CodeCommit / Bitbucket / etc...)
- A testing / build server checks the code as soon as it's pushed (CodeBuild / Jenkins CI / etc...)
- The developer gets feedback about the tests and checks that have passed / failed

**[Overall]**
- Find bugs early, fix bugs
- Deliver faster as the code is tested
- Deploy often
- Happier developers, as they're unblocked

<img src="https://user-images.githubusercontent.com/86287920/185819995-77f33331-a56a-4904-8539-acfe9ae7675f.png">

### Continuous Delivery
- Ensure that the software can be released reliably whenever needed
- Ensures deployments happen often and are quick
- Shift away from "one release every 3 months" to "5 releases a day"
- That usally means automated deployment
   - Code Deploy
   - Jenkins CD
   - Spinnaker
   - Etc...

<img src="https://user-images.githubusercontent.com/86287920/185819996-44cd6c8a-5eec-46bd-8533-bb6ec6087539.png">
