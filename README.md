# CSYE6225 Infrastructure

**Name**  - Sujaykumaran Palanikumar Sankarapandian<br/>
**NUID**  - 002108932<br/>
**Email** - palanikumarsankara.s@northeastern.edu 

## Description:

The Infrastructure YAML file,<br/>
1. Creates a Virtual Private Cloud (VPC).
2. Creates 3 subnets, each in a different availability zone in the same region in the same VPC.
3. Creates an Internet Gateway resource and attaches the Internet Gateway to the VPC.
4. Creates a public route table. Attaches all subnets created to the route table.
5. Creates a public route in the public route table created above with destination CIDR block 0.0.0.0/0 and internet gateway created above as the target.

## Instructions to Run:

1. Configure AWS CLI. 
2. Import SSL certificate in AWS.
3. Clone this repository using the 'git clone' command. 'cd' into the repository.
4. Run the Command 'aws cloudformation create-stack --stack-name myvpc --template-body file://csye6225-infra.yml' to create the Stack.
5. You can see the Stack being created in the AWS Console under CloudFormation.
6. Run the command 'aws cloudformation delete-stack –stack-name myvpc' to cleanup the Stack.

## Command to Import SSL Certificate:
aws acm import-certificate --certificate fileb://certificate.pem --certificate-chain fileb://demo_sujay_me.ca-bundle --private-key fileb://PrivateKey.pem