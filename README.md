# Securing workload in IBM Cloud VPC. 

Applications in Cloud environment needs an enterprise level security and protection. There are number of security standards, deployment patterns, cloud security tools and services available in IBM Cloud to deliver a secure application environment. IBM Cloud Services provides the following security services and capbilities to build a secure platform for applications:
1. Virtual security appliances
2. Hub-spoken deployment model
3. VPC Security group & access control 
4. Security & compliance center
5. Monitoring and Logging
6. Event notification
7. Encryption
8. IAM userid and access group management 

There are few different patterns and products that can be used for deployment in IBMM Cloud such as:


## 1- Single VPC , HA Palo Alto instance, web HA-VSI app:
The purpose of this pattern to deploy single VPC and HA Palo Alto instances in one region to protect a web facing VSI cluster application.
Components of this solution:
1. Single VPC in single region
2. Public ALB internet facing for internet facing application
3. HA Palo Alto virtual instance in VPC
4. Auto-scale Web application on VSIs in VPC with instance group
5. Private ALB internal facing for Auto-scale

The following link describe steps for using available terraform for this pattern:

https://github.com/bkoohi/vpc-ha-pa-vsi-app

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
