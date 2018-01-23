
# VPC-Scenario2

Amazon's [VPC Scenario 2](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario2.html) is the classic network architecture. It can support public-facing and private components.


## Pre-installation steps

Upload the required plugins:

  ** [AWSSDK Plugin](https://github.com/cloudify-incubator/cloudify-awssdk-plugin/releases).

__Check the blueprint for the exact version of the plugin.__


## Installation

On your Cloudify Manager, navigate to `Local Blueprints` select `Upload`.

Once you see the new `blueprint`, "aws", select `Deploy`.

Navigate to `Deployments`, select the "aws" `deployment`, select `Execute Workflow` button and select `Install`.
