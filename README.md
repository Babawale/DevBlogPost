### Blog Title - Managing Rolling Updates in AWS Auto Scaling Groups with AWS CloudFormation Update Policy
This folder contains the CloudFormation codes used in the blog post.


#### [network-infra.yaml](network-infra.yaml)
Deploys the network infrastructure.

#### [network-infra-params.json](network-infra-params.json)
Parameters for the network infrastructure

In YAML code, the `${EnvironmentName}` would be substituted with `BlogPostDemo` accordingly.

#### [servers-without-update-policy.yaml](servers-without-update-policy.yaml)
Deploys the web servers with no Update Policy defined on the ASG

#### [servers-with-update-policy.yaml](servers-with-update-policy.yaml)
Includes an Update Policy for the ASG and signal response capability

#### [projectservers-params.json](servers-params.json)
Parameters for the web servers

#### [create.sh](create.sh)
Helper script to create the CloudFormation stack.
For example, to create a network stack named 'infra` in US-EAST-1 using the network-infra.yaml template file and network-infra-params.json parameter file, use
 
`./create.sh infra network-infra.yaml network-infra-params.json us-east-1`

#### [update.sh](update.sh)
Helper script to update the CloudFormation stack.

`./update.sh servers servers-with-update-policy.yaml servers-params.json us-east-1`
#### [delete.sh](delete.sh)
Helper script to delete the CloudFormation stack
For example, to delete the server stack,
`./delete.sh servers us-east-1`
