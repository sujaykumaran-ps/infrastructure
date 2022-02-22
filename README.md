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
2. Clone this repository using the 'git clone' command. 'cd' into the repository.
3. Run the Command 'aws cloudformation create-stack --stack-name myvpc --template-body file://csye6225-infra.yml' to create the Stack.
4. You can see the Stack being created in the AWS Console under CloudFormation.
5. Run the command 'aws cloudformation delete-stack –stack-name myvpc' to cleanup the Stack.