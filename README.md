# Create ubuntu AMI with nginx in AWS

### Setup Instructions

##### 1.	Install Packer - https://learn.hashicorp.com/tutorials/packer/get-started-install-cli
##### 2.	Authenticate to AWS
>    -	Before you can build the AMI, you need to provide your AWS credentials to Packer as environment variables. You can create AWS credentials on this page. These credentials have permissions to create, modify and delete EC2 instance s. Refer to the documentation to find the full list IAM permissions required to run the amazon-ebs builder.
>    -	Add your AWS credentials as two environment variables, AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY, replacing YOUR_ACCESS_KEY and YOUR_SECRET_KEY with their respective values.

        export AWS_ACCESS_KEY_ID=YOUR_ACCESS_KEY
        export AWS_SECRET_ACCESS_KEY=YOUR_SECRET_KEY
>    -	You may need to also export your AWS_SESSION_TOKEN and AWS_SESSION_EXPIRATION as environment variables.
##### 3.	Clone the repo.
##### 4.	Run the following commands in the cloned folder:
>    -	packer init .  – Packer will download the plugin. In our case packer will download the Packer Amazon plugin that is greater than version 0.0.2.
>    -	packer fmt . – Updates templates in the current directory for readability and consistency. 
>    -	packer validate . – Validates the template. If Packer detects any invalid config, It will print out the file name, the error type and line number of the invalid configuration.
>    -	packer build . – It will build the image.
