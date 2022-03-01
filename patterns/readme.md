

## 2- Single VPC , HA Palo Alto instances , IKS app :
The purpose of this pattern to deploy single VPC and HA Palo Alto instances in one region to protect a web facing VSI application.
Components of this solution:
1. Single VPC in single region
2. Public ALB internet facing for internet facing application
3. HA Palo Alto virtual instance in VPC
4. IKS Container application in VPC 
5. Private ALB internal facing for Auto-scale

The following link describe steps for using available terraform for this pattern:

https://github.com/bkoohi/vpc-ha-pa-iks-app


## 3- Hub-Spoken VPCs , HA Palo Alto instances in Hub VPC, IKS app in Spoken VPC:
The purpose of this pattern to deploy a HUB VPC for HA Palo Alto instances and a Spoken VPC for IKS container app. 

Components of this solution:
1. HUB VPC in single region
2. Public ALB internet facing for internet facing application
3. HA Palo Alto virtual instance in the HUB VPC
4. Spoken VPC in the same region 
5. IKS cluster with container application in the Spoken VPC 

The following link describe steps for using available terraform for this pattern:

https://github.com/bkoohi/hub-spoken-vpc-ha-pa-iks-app
