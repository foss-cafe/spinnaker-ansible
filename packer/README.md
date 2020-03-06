# Spinnaker AMI Image

Spinnaker Base AMI image for spinning up standalone spinnaker server

### Install Packer

Download latest version of Packer (>~1.5.x)
https://www.packer.io/downloads.html

### Input variables

| Name              | Description                      | Default Value           |
| ----------------- | -------------------------------- | ----------------------- |
| ami_region        | Region to build AMI Image        | us-west-2               |
| ami_instance_type | Type of instance used for Packer | t2.medium               |
| ami_ssh_username  | Default SSH remote username      | ubuntu                  |
| ami_name          | AMI image name for tagging       | spinnaker               |
| ami_description   | AMI Image Description            | Spinnaker HAL ami image |

### Run Packer

```bash
packer validate -var-file=variables.json ami.json

packer build -var-file=variables.json ami.json
```

#### Code for moving to Private Subnet Block

```json
      "ssh_interface": "private_ip",
      "subnet_filter": {
        "filters": {
          "tag:Tier": "master*"
        },
        "most_free": true
      }
```

### To-Do

- [ ] Move Packer build to private Subnet
