
## 1- Single VPC , HA Palo Alto instance, web HA-VSI app:
The purpose of this pattern to deploy single VPC and HA Palo Alto instances in one region to protect a web facing VSI cluster application.
Components of this solution:
1. Single VPC in single region
2. Public ALB internet facing for internet facing application
3. HA Palo Alto virtual instance in VPC
4. Auto-scale Web application on VSIs in VPC with instance group
5. Private ALB internal facing for Auto-scale

The following link describe steps for using available terraform for this pattern:
