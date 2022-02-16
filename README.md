# This repository creates Amazon Machine Image with ubuntu OS and nginx on it using Packer

### Prerequisites

- Packer (version >=1.5) Check [here](https://learn.hashicorp.com/tutorials/packer/get-started-install-cli) for install instructions.
- AWS subscription

### Setup Instructions

#### I. Clone the repo

```
$ git clone https://github.com/krasteki/packer-ubuntu-nginx-AWS-box.git
```

#### II. Authenticate to AWS

```
$ export AWS_ACCESS_KEY_ID=YOUR_ACCESS_KEY
$ export AWS_SECRET_ACCESS_KEY=YOUR_SECRET_KEY
```

**Note**: You may need to also export your `AWS_SESSION_TOKEN` and `AWS_SESSION_EXPIRATION` as **environment variables**.

#### III. Run the following commands in the cloned folder:

1. `$ packer init` – Packer will download the plugin. In our case packer will download the Packer Amazon plugin that is greater than version 0.0.2.
2. `$ packer fmt` – Updates templates in the current directory for readability and consistency. 
3. `$ packer validate` – Validates the template. If Packer detects any invalid config, It will print out the file name, the error type and line number of the invalid configuration.
4. `$ packer build`  – It will build the image.
