# node4lambda

Getting started with a NodeJS project on AWS Lambda

1. Git repo on AWS CodeCommit
2. Add SSH key to AWS IAM user
3. Add policies to AWS IAM user:
    * IAMUserSSHKeys
    * IAMReadOnlyAccess
    * AWSCodeCommitFullAccess
4. Express.js skeleton project
    * GitIgnore: https://github.com/github/gitignore/blob/master/Node.gitignore
5. Create pipeline in AWS CodePipeline
    * Add AWS CodeBuild w/image: aws/codebuild/nodejs:7.0.0
    * Add AWS CloudFormation
      * Action: create or update stack
      * Capability: CAPABILITY_IAM
    * Add buildspec.yml
6. Configure AWS CloudFormation
    * template.json
      * http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-lambda.html
    * configuration.json
      * http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/continuous-delivery-codepipeline-action-reference.html
      
1. Restart #4 
   * http://docs.aws.amazon.com/lambda/latest/dg/automating-deployment.html
     * Add index.js
     * Add samTemplate.yml
   * Add a role in AWS IAM
     * Role Type: AWS CloudFormation
     * Attach Policy: AWS Lambda Execute
     * Inline Role Policy: (Copy and paste)
   
   