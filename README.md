
# VPC-Scenario2

Amazon's [VPC Scenario 2](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario2.html) is the classic network architecture. It can support public-facing and private components.


## Pre-installation steps


Upload the [required plugin](https://github.com/cloudify-incubator/cloudify-awssdk-plugin/releases).


![Upload Required Plugin][uploadplugin]


__Check the blueprint for the exact version of the plugin.__


## Installation


Download the latest [zip archive](https://github.com/cloudify-examples/vpc-scenario2-blueprint/archive/master.zip).


![Download Latest Zip Archive][downloadarchive]


Navigate to `Local Blueprints` and `Upload` the `blueprint` archive to your manager.


![Upload Blueprint Archive][uploadblueprint]


Once you see the new `blueprint`, "aws", select `Deploy`.


![Create Deployment][createdeployment]


Navigate to `Deployments`, select the "aws" `deployment`, select `Execute Workflow` button and select `Install`.


![Execute Install Workflow][installworkflow]


[uploadplugin]: https://github.com/cloudify-examples/vpc-scenario2-blueprint/releases/download/images/uploadplugin.png "Upload Plugin"
[downloadarchive]: https://github.com/cloudify-examples/vpc-scenario2-blueprint/releases/download/images/downloadarchive.png "Download Archive"
[uploadblueprint]: https://github.com/cloudify-examples/vpc-scenario2-blueprint/releases/download/images/uploadblueprint.png "Upload Blueprint"
[createdeployment]: https://github.com/cloudify-examples/vpc-scenario2-blueprint/releases/download/images/createdeployment.png "Create deployment"
[installworkflow]: https://github.com/cloudify-examples/vpc-scenario2-blueprint/releases/download/images/installworkflow.png "Execute Install"
