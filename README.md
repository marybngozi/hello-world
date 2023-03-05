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

## By MaryBlessing Umeh
