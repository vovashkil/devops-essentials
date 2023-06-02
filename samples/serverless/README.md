# Serverless Examples
Serverless Examples. This solution is based on [Continuous Deployment for Serverless Applications
](https://aws.amazon.com/blogs/compute/continuous-deployment-for-serverless-applications/)

# Overview
This repo is a demonstration of Continuous Delivery of a static website to AWS Lambda, API Gateway, and others via CodePipeline, CodeCommit, CodeBuilds. Ensure you've configured the [Prerequisites](https://github.com/stelligent/devops-essentials/wiki/Prerequisites) before launching the stack below.

# Launch Stack

[![Launch CFN stack](https://s3.amazonaws.com/www.devopsessentialsaws.com/img/deploy-to-aws.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#cstack=sn%7Edevops-essentials-serverless%7Cturl%7Ehttps://s3.amazonaws.com/www.devopsessentialsaws.com/samples/serverless/pipeline.yml)
# Configure Solution

1. Once the CloudFormation stack is successful, select the checkbox next to the stack and click the <strong>Outputs</strong> tab. 
1. From Outputs, click on the **PipelineUrl** output. The Source action will be in a failed state.
1. From the CodePipeline Source action, click on the CodeCommit provider and copy the **git clone** statement provided by CodeCommit
1. Paste the command in your Terminal
1. From [this](../serverless) folder, copy the **codecommit** folder to your locally cloned Git repo
1. From your Terminal, type `git add .`
1. From your Terminal, type `git commit -am "add new files"`
1. From your Terminal, type `git push`
1. Go back to your pipeline in CodePipeline and see the changes flow through the pipeline
1. Once the pipeline is complete, go to your CloudFormation Outputs and click on the **SiteUrl** Output

# Resources

1. The CloudFormation template is available [here](https://s3.amazonaws.com/www.devopsessentialsaws.com/samples/serverless/pipeline.yml).