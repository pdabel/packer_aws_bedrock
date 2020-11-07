# setup AWS image for running Minecraft Bedrock edition on Ubuntu

* Checkout code and save to local directory
* download latest Ubuntu edition from Minecraft https://www.minecraft.net/en-us/download/server/bedrock, save in this directory
* Setup AWS account and create access/secret key
* run validation code
```bash
packer validate bedrock.json
```
* run build
```bash
packer build \
    -var 'aws_access_key=<AWS_ACCESS_KEY>' \
    -var 'aws_secret_key=<AWS_SECRET_KEY>' \
    bedrock.json