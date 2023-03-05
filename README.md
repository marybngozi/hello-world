# Hello CICD Configure and deployment

Infrastructure creation and configuration with ansible

## Setup

### Get EC2 Public Ip address and add to inventory file

```
aws ec2 describe-instances --query 'Reservations[*].Instances[*].PublicIpAddress' --filters "Name=tag:Project,Values=udacity" --output text >> inventory.txt
```

```
aws ec2 describe-instances --query 'Reservations[*].Instances[*].PublicIpAddress' --filters --output text >> inventory.txt
```

## Add deployment script and green-blue routing

### cloudfront.yml

- PipelineID - Name of the S3 bucket you created manually.

```
aws cloudformation deploy \
--template-file cloudfront.yml \
--stack-name production-distro \
--parameter-overrides PipelineID="mybuck10988483202"
```

## By MaryBlessing Umeh
