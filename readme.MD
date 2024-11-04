# Terraform AWS VPC Module customised

This module is going to create the following resources for HA[high availability] we are going to get first 2 AZ[avialability zones]

* VPC 
* Internet Gate way associated with vpc
* 2 Public subnets
* 2 Private subnets
* 2 Database subnets
* Database subnet group
* EIP
* NAT Gate way 
* Public Route Table
* Private Route Table 
* Database Route table
* Routes
* Route Table associations with subnets
* Peering with default VPC (if required)
* Peering Routes in Accepter and Requester Route tables

# Inputs

* project_name (mandatory) : User must supply their project name
* environment (mandatory) : User must supply their environment name
* vpc_cidr (mandatory) : User must supply their VPC CIDR
* enable_dns_hostnames (optional) : defaults to true
* common_tags (optional) : Default is empty. User can supply tags in map(string) format
* vpc_tags (optional) : Default is empty. User can supply tags in map(string) format
* igw_tags (optional) : Default is empty. User can supply tags in map(string) format
* public_subnet_cidr (mandatory) : User must supply only 2 valid public subnet CIDR
* public_subnet_tags (optional) : Default is empty. User can supply tags in map(string) format
* private_subnet_cidr (mandatory) : User must supply only 2 valid private subnet CIDR
* private_subnet_tags (optional) : Default is empty. User can supply tags in map(string) format
* database_subnet_cidr (mandatory) : User must supply only 2 valid Database subnet CIDR
* database_subnet_tags (optional) : Default is empty. User can supply tags in map(string) format
* db_subnet_group_tags (optional) : Default is empty. User can supply tags in map(string) format
* nat_gateway_tags (optional) : Default is empty. User can supply tags in map(string) format
* public_route_table_tags (optional) : Default is empty. User can supply tags in map(string) format
* private_route_table_tags (optional) : Default is empty. User can supply tags in map(string) format
* database_route_table_tags (optional) : Default is empty. User can supply tags in map(string) format
* is_peering_required (optional) : Default is empty. User can supply tags in map(string) format 
* vpc_peering_tags (optional) : Default is empty. User can supply tags in map(string) format

# Outputs
 
* vpc_id : VPC ID created
* public_subnet_ids : List of 2 Public Subnet ids created
* private_subnet_ids :  List of 2 Private Subnet ids created
* database_subnet_ids : List of 2 Database Subnet ids created  