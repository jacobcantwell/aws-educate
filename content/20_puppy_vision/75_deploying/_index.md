+++
title = "Deploying"
chapter = true
weight = 75
+++

## Deploying the model

You trained model is now ready to integrate into a website, software applications, mobile phone apps, any way that you think you can use it.

We will deploy a demonstration web application that you can use to test Custom Labels with models trained by Amazon Rekognition.

### Architecture

The Custom Labels Demo uses [Amazon Rekognition](https://aws.amazon.com/rekognition) for label recognition, [Amazon Cognito](https://aws.amazon.com/cognito) for authenticating the Service Requests, and [Amazon CloudFront](https://aws.amazon.com/cloudfront), [Amazon S3](https://aws.amazon.com/s3), [AWS Amplify](https://aws.amazon.com/amplify), and [React](https://reactjs.org) for the front-end layer.

![Architecture Diagram](75_deploying/images/amazon-rekognition-1.png)

When accessing the Demo, the frontend app calls the `DescribeProjects` action in Amazon Rekognition. Then, for each project, it calls the `DescribeProjectVersions` action. This is for fetching the list and status of each model in the current account.

In addition to showing all the models, the UI allows to start all the models in the *TRAINING_COMPLETED* or *STOPPED* state by calling the `StartProjectVersion` action.
The UI also allows to stop a model in the *RUNNING* state by calling the `StopProjectVersion` action.

If you have any model in the *RUNNING* state, you can click the title and then select an image from your local machine to detect custom labels. The frontend app will call the `DetectCustomLabels` action in Amazon Rekognition.

To learn more about Custom Labels [consult the documentation](https://docs.aws.amazon.com/rekognition/latest/customlabels-dg/what-is.html).

### Usage

#### Prerequisites

Your access to the AWS account must have IAM permissions to launch AWS CloudFormation templates that create IAM roles.

#### Deployment

The demo application is deployed as an [AWS CloudFormation](https://aws.amazon.com/cloudformation) template.

> **Note**

You are responsible for the cost of the AWS services used while running this sample deployment. There is no additional cost for using this sample. For full details, see the following pricing pages for each AWS service you will be using in this sample.  Prices are subject to change.

> * [Amazon Rekognition Pricing](https://aws.amazon.com/rekognition/pricing/)
> * [Amazon S3 Pricing](https://aws.amazon.com/s3/pricing/)
> * [Amazon Cognito Pricing](https://aws.amazon.com/cognito/pricing/)
> * [Amazon CloudFront Pricing](https://aws.amazon.com/cloudfront/pricing/)

1. Deploy the latest CloudFormation template by following the link below for your preferred AWS region:

|Region|Launch Template|
|------|---------------|
|**US East (N. Virginia)** (us-east-1) | [![Launch the CustomLabelsDemo Stack with CloudFormation](75_deploying/images/deploy-to-aws.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=CustomLabelsDemo&templateURL=https://solution-builders-us-east-1.s3.us-east-1.amazonaws.com/amazon-rekognition-custom-labels-demo/latest/template.yaml)|
|**US East (Ohio)** (us-east-2) | [![Launch the CustomLabelsDemo Stack with CloudFormation](75_deploying/images/deploy-to-aws.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-2#/stacks/new?stackName=CustomLabelsDemo&templateURL=https://solution-builders-us-east-2.s3.us-east-2.amazonaws.com/amazon-rekognition-custom-labels-demo/latest/template.yaml)|
|**US West (Oregon)** (us-west-2) | [![Launch the CustomLabelsDemo Stack with CloudFormation](75_deploying/images/deploy-to-aws.png)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=CustomLabelsDemo&templateURL=https://solution-builders-us-west-2.s3.us-west-2.amazonaws.com/amazon-rekognition-custom-labels-demo/latest/template.yaml)|
|**EU (Ireland)** (eu-west-1) | [![Launch the CustomLabelsDemo Stack with CloudFormation](75_deploying/images/deploy-to-aws.png)](https://console.aws.amazon.com/cloudformation/home?region=eu-west-1#/stacks/new?stackName=CustomLabelsDemo&templateURL=https://solution-builders-eu-west-1.s3.eu-west-1.amazonaws.com/amazon-rekognition-custom-labels-demo/latest/template.yaml)|


1. If prompted, login using your AWS account credentials.

2. You should see a screen titled "*Create Stack*" at the "*Specify template*" step. The fields specifying the CloudFormation template are pre-populated. Click the **Next** button at the bottom of the page.

3. On the "*Specify stack details*" screen you may customize the following parameters of the CloudFormation stack:
   * **Stack Name:** (Default: *CustomLabelsDemo*) This is the name that is used to refer to this stack in CloudFormation once deployed. The value must be 15 characters or less.
   * **AdminEmail:** This is the e-mail address used to create the Admin User in the Cognito User Pool.
   * **ResourcePrefix:** (Default: *RekogCustomLabelsDemo*) AWS Resources are named based on the value of this parameter. You must customise this if you are launching more than one instance of the stack within the same account.
   * **CreateCloudFrontDistribution**  (Default: *true*) Creates a CloudFront distribution for accessing the web interface of the demo. This must be enabled if S3 Block Public Access is enabled at an account level. **Note:** Creating a CloudFront distribution may significantly increase the deploy time (from approximately 5 minutes to over 30 minutes).

   When completed, click **Next**

4. [Configure stack options](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-add-tags.html) if desired, then click **Next**.
5. On the review you screen, you must check the boxes for:

   * "*I acknowledge that AWS CloudFormation might create IAM resources*" 
   * "*I acknowledge that AWS CloudFormation might create IAM resources with custom names*"
   * "*I acknowledge that AWS CloudFormation might require the following capability: CAPABILITY_AUTO_EXPAND*"

   These are required to allow CloudFormation to create the IAM roles specified in the CloudFormation using both fixed and dynamic names.
   
6. Click **Create Change Set**
7. On the *Change Set* screen, click **Execute** to launch your stack.
   * You may need to wait for the *Execution status* of the change set to become "*AVAILABLE*" before the "**Execute**" button becomes available.

8. Wait for the CloudFormation stack to launch. Completion is indicated when the "Stack status" is "*CREATE_COMPLETE*".
   * You can monitor the stack creation progress in the "Events" tab.
9.  Note the *url* displayed in the *Outputs* tab for the stack. This is used to access the application.

#### Accessing and using the Demo

Once deployed, the application can be accessed using a web browser using the address specified in `url` output from the CloudFormation stack created during [deployment](#deployment) of the solution.

When accessing the application for the first time, you need to use the Admin e-mail provided during Stack Creation as username. A temporary password will be sent to the same e-mail address. After authentication, it will be necessary to create a new password and click "Change".

To manage users, you can use the [Cognito Users Pool console](https://console.aws.amazon.com/cognito/users).

