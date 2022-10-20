# infrastructure

### Clone the repository

git clone git@github.com:Pratik-Hariya-002929941/infrastructure.git
cd infrastructure

### Configure profile

aws configure --profile dev

### Create Stack

aws cloudformation deploy --profile dev --template-file csye6225-infra.yml --stack-name Stack6225

### Check Stacks

aws cloudformation describe-stacks --profile dev

### Delete Stack

aws cloudformation delete-stack --stack-name Stack6225 --profile dev

### Create Stack with Parameter
aws cloudformation --profile demo create-stack --stack-name Stack6225 --template-body file://csye6225-infra.yml --parameter ParameterKey=VirtualPrivateCloud,ParameterValue="10.0.0.0/16" ParameterKey=PublicSubnet1,ParameterValue="10.0.1.0/24" ParameterKey=PublicSubnet2,ParameterValue="10.0.2.0/24" ParameterKey=PublicSubnet3,ParameterValue="10.0.3.0/24" ParameterKey=ImageValue,ParameterValue="ami-0ed9a9a88a44b2c81"
