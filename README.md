
# VPC-Scenario2

Amazon's [VPC Scenario 2](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario2.html) is the classic network architecture. It can support public-facing and private components.


## Compatibility

Tested with:
  * Cloudify 4.2


## Pre-installation steps

Upload the required plugins:

  * [AWSSDK Plugin](https://github.com/cloudify-incubator/cloudify-awssdk-plugin/releases).

_Check the blueprint for the exact version of the plugin._


If you do not override the default inputs during the `deployments create` phase below, you must have these secrets in your Cloudify Manager `tenant`:

  * aws_access_key_id
  * aws_secret_access_key
  * ec2_region_name, such as `us-east-1`.
  * ec2_region_endpoint, such as `ec2.us-east-1.amazonaws.com`.
  * availability_zone, such as `us-east-1c`.


## Installation

On your Cloudify Manager, navigate to `Local Blueprints` select `Upload`.

Once you see the new blueprint, select `Deploy`.

Navigate to `Deployments`, find your `deployment` select `Install` from the `workflow`'s menu. At this stage, provide your own values for any of the default `inputs` values.


## Uninstallation

Navigate to the deployment and select `Uninstall`.
