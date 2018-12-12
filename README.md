
# AWS Example Network

Amazon's [VPC Scenario 2](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario2.html) is the classic network architecture. It can support public-facing and private components.

### Resources Created

  * A `vpc`.
  * An `internet_gateway`.
  * A `public_subnet`.
  * A `private_subnet`.
  * A `public_subnet_routetable`.
  * A `private_subnet_routetable`.
  * A `route_public_subnet_internet_gateway`.
  * A `nat_gateway_ip` - created with the `update-blueprint.yaml`.
  * A `nat_gateway` - created with the `update-blueprint.yaml`.
  * A `route_private_subnet_nat_gateway` - created with the `update-blueprint.yaml`.


## Compatibility

Tested with:
  * Cloudify 4.5


## Pre-installation steps

Upload the required plugins:

  * [AWSSDK Plugin](https://github.com/cloudify-incubator/cloudify-awssdk-plugin/releases).

_Check the blueprint for the exact version of the plugin._


If you do not provide your own `deployment inputs` below, you must add these secrets to your Cloudify Manager `tenant`:

  * `aws_access_key_id`
  * `aws_secret_access_key`
  * `ec2_region_name`, such as `us-east-1`.
  * `ec2_region_endpoint`, such as `ec2.us-east-1.amazonaws.com`.
  * `availability_zone`, such as `us-east-1c`.


## Installation

On your Cloudify Manager, navigate to `Local Blueprints` select `Upload`.

[Right-click and copy URL](https://github.com/cloudify-examples/aws-example-network/archive/master.zip). Paste where it says `Enter blueprint url`. Provide a blueprint name, such as `examples-network` in the field labeled `blueprint name`. Select `simple-blueprint.yaml` from `Blueprint filename` menu.

After the new blueprint has been created, click the `Deploy` button.

Navigate to `Deployments`, find your new deployment, select `Install` from the `workflow`'s menu. At this stage, you may provide your own values for any of the default `deployment inputs`.


## Update Deployment

### Stage 1
In order to provide outbound internet access to the private subnet, you can update the deployment.

Navigate to `Deployments`, find your deployment, click on it. Once the deployment's page has loaded, click the `Update Deployment` button. [Right-click and copy URL](https://github.com/cloudify-examples/aws-example-network/archive/master.zip). Paste where it says `Enter new blueprint url`. This time, select `update-blueprint.yaml` from `Blueprint filename` menu.

### Stage 2

This update deployment stage will add support to the following:
 - VPN Connection to old vpc `vpc_1` node
 - VPC Peering between two vpc `vpc_1` & `vpc_2`

Navigate to `Deployments`, find your deployment, click on it. Once the deployment's page has loaded, click the `Update Deployment` button. [Right-click and copy URL](https://github.com/cloudify-examples/aws-example-network/archive/master.zip). Paste where it says `Enter new blueprint url`. This time, select `vpc-peering-blueprint.yaml` from `Blueprint filename` menu.

## Uninstallation

Navigate to the deployment and select `Uninstall`. When the uninstall workflow is finished, select `Delete deployment`.
