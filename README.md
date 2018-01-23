
# VPC-Scenario2

Amazon's [VPC Scenario 2](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario2.html) is the classic network architecture. It can support public-facing and private components.


## Pre-installation steps

Upload the required plugins:

  * [AWSSDK Plugin](https://github.com/cloudify-incubator/cloudify-awssdk-plugin/releases).

**Check the blueprint for the exact version of the plugin.**


If you do not override the default inputs, these are required as secrets:

  * aws_access_key_id
  * aws_secret_access_key
  * ec2_region_name, such as `us-east-1`.
  * ec2_region_endpoint, such as `ec2.us-east-1.amazonaws.com`.
  * availability_zone, such as `us-east-1c`.


## Installation

On your Cloudify Manager, navigate to `Local Blueprints` select `Upload`.

Once you see the new `blueprint`, "aws", select `Deploy`.

Navigate to `Deployments`, select the "aws" `deployment`, select `Execute Workflow` button and select `Install`.


## Uninstallation

Navigate to the `aws` deployment and select `Uninstall`.
