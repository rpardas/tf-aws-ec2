## Terraform for building an EC2 instance

### Install and set up

#### AWS CLI

[AWS CLI Install Instructions](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

Export environment variables for your access keys

`export AWS_ACCESS_KEY_ID=`

`export AWS_SECRET_ACCESS_KEY=`

#### Terraform

[Hahicorp Instructions](https://developer.hashicorp.com/terraform/install)

Mac example

`brew tap hashicorp/tap`

`brew install hashicorp/tap/terraform`

### Create the infrastructure

Note: This project creates an instance in the `us-west-2` region.

#### Intialize

`terraform init`

#### Format the configuration

`terraform fmt`

#### Validate the configuration

`terraform validate`

#### Apply the configuration

`terraform apply`

#### Verification

Check for the new instance in [EC2 console](https://console.aws.amazon.com/ec2/v2/home?region=us-west-2#Instances:sort=instanceId).

Inspect the `terraform.tfstate` file.

and/or

`terraform show`

List resources in the project's state

`terraform state list`

#### Making changes

Update `main.tf`. For instance: change the `ami` within `resource`.

Apply the changes.

`terraform apply`

Watch the output for changes made and see the updated instance.

#### Destroy

`terraform destroy`

Check for the terminated instance(s).

