# Welcome to your CDK TypeScript project

This is a sample project for CDK development with TypeScript.

The `cdk.json` file tells the CDK Toolkit how to execute your app.

## Useful commands

* `npm run build`   compile typescript to js
* `npm run watch`   watch for changes and compile
* `npm run test`    perform the jest unit tests
* `cdk deploy`      deploy this stack to your default AWS account/region
* `cdk diff`        compare deployed stack with current state
* `cdk synth`       emits the synthesized CloudFormation template

## What's it ?
By running `cdk init`, it creates a number of files and folders inside your parent directory to help you organize the source code of your AWS CDK app.
- If you have GIT installed, each project you create using `cdk init` is also initialized as a `git` repository.

### Build the app
- By running `cdk build`, however this isnt strictly necessary with the AWS CDK- the toolkit does it for you so that you cant forgot. you can still build manually by running the above command.

### List stack available
 RUn the command `cdk ls`
 - the command list available stack.

 ### Add an S3 bucket
 - in the `lib/hello-typescript-cdk-stack.ts` edit and add S3 as follows
 <code>
    new s3.Bucket(this, 'MyFirstBucket', {
    versioned: true,
    });
 </code>

### Synthesize an AWS CloudFormation template
`cdk synth`
By synthesizing the resources defined in it will be translated into an AWS Cloudformation template. The displayed output of the `cdk synth` is YAML-format template.
- The template is saved in the `cdk.out` directory in JSON format.

### Deploy the stack
To deploy the stack using AWS Cloudformation, issue: `cdk deploy`

### You can modify and see the changes
By isuing the command: `cdk diff`

### Destroying the app resource
By running the command `cdk destroy`