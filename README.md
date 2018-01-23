
# VPC-Scenario2

Amazon's [VPC Scenario 2](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario2.html) is the classic network architecture. It can support public-facing and private components.


## Compatibility

Tested with:
  * Cloudify 4.2


## Pre-installation steps

Upload the required plugins:

  * [AWSSDK Plugin](https://github.com/cloudify-incubator/cloudify-awssdk-plugin/releases).

_Check the blueprint for the exact version of the plugin._


If you do not provide your own `deployment inputs` below, you must add these secrets to your Cloudify Manager `tenant`:

  * aws_access_key_id
  * aws_secret_access_key
  * ec2_region_name, such as `us-east-1`.
  * ec2_region_endpoint, such as `ec2.us-east-1.amazonaws.com`.
  * availability_zone, such as `us-east-1c`.


## Installation

On your Cloudify Manager, navigate to `Local Blueprints` select `Upload`.

_Hint: You may provide the URL to the github archive, [right-click and copy URL](https://github.com/cloudify-examples/vpc-scenario2-blueprint/archive/master.zip), or download the archive and provide the archive as an attachment to upload._

After the new blueprint has been created, select `Deploy`.

Navigate to `Deployments`, find your new deployment, select `Install` from the `workflow`'s menu. At this stage, you may provide your own values for any of the default `deployment inputs`.


## Uninstallation

Navigate to the deployment and select `Uninstall`.
