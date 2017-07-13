# ECSCloudFormation
This app has 2 containers on each ec2 instance. The front end public website talks to a back end api on the same instance.

The repository consists of a set of nested templates that deploy the following:
	• A tiered VPC with public and private subnets, spanning an AWS region.
	• A highly available ECS cluster deployed across two Availability Zones in an Auto Scaling group.
	• A pair of NAT gateways (one in each zone) to handle outbound traffic.
	• Two interconnecting microservices deployed as ECS services (website-service and product-service).
	• An Application Load Balancer (ALB) to the public subnets to handle inbound traffic.
	• ALB path-based routes for each ECS service to route the inbound traffic to the correct service.
        . Centralized container logging with Amazon CloudWatch Logs.


Modify the templates.
Upload them to an Amazon S3 bucket of your choice.
Either create a new CloudFormation stack by deploying the master.yaml template, or update your existing stack with your version of the templates.

This app has 2 containers on each ec2 instance. The front end public website talks to a back end api on the same instance.

Dockerize an image push to the AWS ECR repository
Update the ContainerName and Image parameters to point to the container image instead of the currrent container.

You have a automated clustred microservices.
