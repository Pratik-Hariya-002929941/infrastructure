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
