# Route Tables

## VPC-1 public route table (associated with public-subnet)
- 10.0.0.0/16 -> local
- 0.0.0.0/0 -> Internet Gateway (my-igw)

## VPC-1 private route table (nat-rt) (associated with private-subnet)
- 10.0.0.0/16 -> local
- 0.0.0.0/0 -> NAT Gateway (my-nat)
- 11.0.0.0/16 -> VPC Peering (my-pc / pcx-...)

## VPC-2 route table (associated with private-subnet-2)
- 11.0.0.0/16 -> local
- 10.0.0.0/16 -> VPC Peering (my-pc / pcx-...)
