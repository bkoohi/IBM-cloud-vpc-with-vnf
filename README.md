# Securing Kubenetes workload in IBM Cloud VPC with Palo Alto. 

Container applications in any Cloud environment needs enterprise level security and protection. Majority of customers have security firewall standards using products and services such as Palo Alto, Checkpoints, Fortigate and other firewall products. It's benefifcial for custoers to use their current security firewall standards for workloads running in Cloud. 

Deploying virtual security services in Cloud and virtual network is different from physical security products in on-premises. The goal of this articiale is to described tested and proven pattern for deployment and security of container workload in IBM Cloud.

There are few different patterns and products that can be used for deployment in IBMM Cloud such as:


## 1- Single VPC , HA Palo Alto instance, web HA-VSI app:
The purpose of this pattern to deploy single VPC and HA Palo Alto instances in one region to protect a web-facing VSI cluster application.
Components of this solution:
1. Single VPC in single region
2. Public ALB internet facing for internet facing application
3. HA Palo Alto virtual instance in VPC
4. Auto-scale Web application on VSIs in VPC with instance group
5. Private ALB internal facing for Auto-scale

The following link describe steps for using available terraform for this pattern:

https://github.com/bkoohi/vpc-ha-pa-vsi-app


## 2- Hub-Spoken VPCs , HA Palo Alto instances in Hub VPC, IKS app in Spoken VPC:
The purpose of this pattern to deploy single VPC and HA Palo Alto instances in one region to protect a web-facing VSI application.
Components of this solution:
1. Single VPC in single region
2. Public ALB internet facing for internet facing application
3. HA Palo Alto virtual instance in VPC
4. IKS Container application in VPC 
5. Private ALB internal facing for Auto-scale


The following link describe steps for using available terraform for this pattern:

https://github.com/bkoohi/vpc-ha-pa-iks-app


