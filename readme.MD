# Terraform AWS VPC Module customised

This module is going to create the following resources. For HA we are going to get first 2 AZ[availability zones]

* VPC
* Internet Gateway associated with VPC
* 2 Public subnets
* 2 Private subnets
* 2 Database subnets
* Database subnet group
* EIP
* NAT Gateway
* Public route table
* Private route table
* Database route table
* Routes
* Route table associations with subnets
* Peering with default VPC (if required)
* Peering routes in accepter and requester rote tables

# Inputs

* project_name (mandatory) : User must supply their project name
* environment (mandatory) : user must supply their environment name 
* vpc_cidr  (mandatory) : user must supply their vpc CIDR
* enable_dns_hostnames (optional) : defaults to true
* common_tags (optional) : Default is empty , User can supply tags in map (string) format
* vpc_tags (optional) : Default is empty , User can supply tags in map (string) format
* igw_tags (optional) : Default is empty , User can supply tags in map (string) format
* public_subnet_cidrs (mandatory) : User must supply only 2 valid public subnet CIDR
* public_subnet_tags (optional) : Default is empty , User can supply tags in map (string) format
* private_subnet_cidrs (mandatory) : user must supply only 2 valid private subnet CIDR
* private_subnet_tags (optional) : Default is empty , User can supply tags in map (string) format
* Database_subnet_cidrs (mandatory) : user must supply only 2 valid database subnet CIDR
* Database_subnet_tags (optional) : Default is empty , User can supply tags in map (string) format
* db_subnet_group_tags (optional) : Default is empty , User can supply tags in map (string) format
* nat_gateway_tags (optional) : Default is empty , User can supply tags in map (string) format
* public_route_table_tags (optional) : Default is empty , User can supply tags in map (string) format
* private_route_table_tags (optional) : Default is empty , User can supply tags in map (string) format
* database_route_table_tags (optional) : Default is empty , User can supply tags in map (string) format
* is_peering_required (optional) : Defaults to false
* vpc_peering_tags (optional) : Default is empty , User can supply tags in map (string) format

# Outputs
 
* vpc_id : VPC ID created
* public_subnet_ids : list of 2 public subnet ids created
* private_subnet_ids :list of 2 private subnet ids created
* database_subnet_ids : list of 2 database subnet ids created 