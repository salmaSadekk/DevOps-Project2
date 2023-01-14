### Project Title - Deploy a high-availability web app using CloudFormation

Kindly check Diagram.pdf for the diagram requirment

## Scripts

```bash
# create infrastructure network
aws cloudformation create-stack  --stack-name network --region us-east-1 --template-body file://network.yml --parameters file://network-parameters.json
# create Servers
aws cloudformation create-stack  --stack-name project2-servers --region us-east-1 --template-body file://servers.yml --parameters file://server-parameters.json
# update infrastructure network
aws cloudformation update-stack  --stack-name network --region us-east-1 --template-body file://network.yml --parameters file://network-parameters.json
# update Servers
aws cloudformation update-stack --stack-name project2-servers --region us-east-1 --template-body file://servers.yml --parameters file://server-parameters.json
```

## Load Balancer link

http://proje-webap-ek7rc1ssg483-2060505917.us-east-1.elb.amazonaws.com/
