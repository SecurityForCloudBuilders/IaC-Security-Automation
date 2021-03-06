# Example of Infrastructure-as-a-Code Security Automation with Cloud One - Conformity Template Scanner

![](Diagram/Example_of_diagram_architecture.png)

Here is a Cloud Formation template based in the AWS Well-Architected Frramework for tests with Template Scanner:
- CFT Example: Well-architect-ec2-template.yml (https://github.com/fernandostc/IaC-Security-Automation/blob/master/Well-architect-ec2-template.yml)


## VSCode Plugin for Cloud One - Conformity (by Raphael Bottino)
- https://marketplace.visualstudio.com/items?itemName=raphaelbottino.cc-template-scanner

## Gitlab CI file Example for Template Scanner for CloudFormation Templates (gitlab-ci-example.yml)

Using the template scanner from Will Robison (https://github.com/OzNetNerd/Cloud-Conformity-Pipeline-Scanner)

Variable Configuration Needed:

- AWS_ACCESS_KEY_ID
- AWS_DEFAULT_REGION
- AWS_SECRET_ACCESS_KEY
- CC_API_KEY
- CC_REGION
- CC_RISK_LEVEL
- CFN_TEMPLATE_FILE_LOCATION

## GitHub Actions by (Felipe Costa and Raphael Bottino)

- https://github.com/marketplace/actions/cloud-one-conformity-pipeline-scanner

Variable Configuration Needed:

- cc_apikey (Cloud One Conformity API KEY)
- cc_region (Cloud One Conformity account region)
- templatePath (Path of the template to be scanned)
- maxExtreme | maxVeryHigh | maxHigh | maxMedium | maxLow (Choose one or more of the options and set a number of how many violations are accepted)

PS.: ALWAYS use secrets to expose your credentials!

## AWS CodeBuild - buildspec file Example for Template Scanner using CloudFormation Templates (buildspec.yml)

Article with Steps-by-Steps on how to build it -> https://fernando0stc.medium.com/building-iac-pipeline-on-aws-with-security-fully-integrate-48952c3435b7?sk=d1f5556f6463878405d42852ba4a52c5

Using the template scanner from Will Robison (https://github.com/OzNetNerd/Cloud-Conformity-Pipeline-Scanner) - Python

Variable Configuration Needed:

- CC_API_KEY = YOUR API KEY FROM CLOUD ONE - CONFORMITY
- CC_REGION =  REGION SELECTED TO CREATE YOUR CONFORMITY TENANT
- CC_RISK_LEVEL = RISK LEVEL NOT BE ACCEPT
- CFN_TEMPLATE_FILE_LOCATION = YOUR CLOUDFORMATION TEMPLATE PATH
- STACK_NAME = THE CLOUDFORMATION STACK NAME
