DAY 2 AWS

Assignment 1

- Create a vpc not by wizard this time but manually, having 2 public subnets and 2 private subnets and 2 protected subnets.

- setup should be highly available

- Create 1 IGW and 2 NGW in each availability zone and make the appropriate routes in route tables

- Main route will remain intact, instead make 4 route tables

public_route_table 

private_route_table_1 

private_route_table_2 

protected_route_table 

SOLUTIONS

1. Created a VPC manually by :-

- Click on VPC

- Click on My VPC

- Click on Create New VPC

![VPC Second](https://github.com/lovedeepsh/AWS/blob/master/AWS-day2-images/Opstree-VPC-second.png)



2. Created 6 Subnets by :-

- Click on VPC

- Click on Subnets below My VPC

- Created 2 Public Subnets, 2 Private Subnets and 2 Protected Subnets.

![Subnets](https://github.com/lovedeepsh/AWS/blob/master/AWS-day2-images/Opstree-Subnets-6.png)

3. Created 4 Route Table by :-

- Click on VPC

- Click on Route Tables below Subnets

- Created Route tables and assigned to each Subnet

- Public Route Table attached to both Public Subnets

- Protected Route Table attached to both Protected Subnets

- Private Route Table are being created for each Private Subnet

![Route Tables](https://github.com/lovedeepsh/AWS/blob/master/AWS-day2-images/Route-Table-4.png)

4. Created a Internet Gateway :-

- Click on VPC

- Click on Internet Gateways below Route Tables

- Created a Internet Gateway and assigned it to newly created VPC.

![Internet Gateway](https://github.com/lovedeepsh/AWS/blob/master/AWS-day2-images/Opstree-igw-second.png)

