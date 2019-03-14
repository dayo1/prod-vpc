# prod-vpc
This is a Complete VPC
Configuration in this directory creates set of VPC resources which may be sufficient for staging or production.

There are public, private, database, ElastiCache, intra (private w/o Internet access) subnets, and NAT Gateways created in each availability zone.

Usage
To run this example you need to execute:

$ terraform init
$ terraform plan
$ terraform apply
$ terraform destroy

Note that this example may create resources which can cost money (AWS Elastic IP, for example). Run terraform destroy when you don't need these resources.

Outputs
Name	Description
database_subnets	List of IDs of database subnets
elasticache_subnets	List of IDs of elasticache subnets
intra_subnets	List of IDs of intra subnets
nat_public_ips	List of public Elastic IPs created for AWS NAT Gateway
private_subnets	List of IDs of private subnets
public_subnets	List of IDs of public subnets
redshift_subnets	List of IDs of redshift subnets
vpc_endpoint_ssm_dns_entry	The DNS entries for the VPC Endpoint for SSM.
vpc_endpoint_ssm_id	The ID of VPC endpoint for SSM
vpc_endpoint_ssm_network_interface_ids	One or more network interfaces for the VPC Endpoint for SSM.
vpc_id	The ID of the VPC
