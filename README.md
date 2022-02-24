# Securing Kubenetes workload in IBM Cloud VPC with Palo Alto. 

Container applications in any Cloud environment needs enterprise level security and protection. Majority of customers have security firewall standards using products and services such as Palo Alto, Checkpoints, Fortigate and other firewall products. It's benefifcial for custoers to use their current security firewall standards for workloads running in Cloud. 

Deploying virtual security services in Cloud and virtual network is different from physical security products in on-premises. The goal of this articiale is to described tested and proven pattern for deployment and security of container workload in IBM Cloud.

There are few different patterns and products that can be used for deployment in IBMM Cloud such as:


## Single VPC , Single Palo Alto instance:
The purpose of this pattern to deploy single VPC and single Palo Alto instance in one region to protect a web-facing application.


are providing enterVPC would need a full firewall security service that a production workload needs. Our client design objective might be not to expose their application directly to internet without a firewall protection. IBM Cloud provides network and security services such as VPC, ALBs and NFVs such as Palo Alto to meet these objectives.

The architecture in this design provides an automation for deploying mutltiple applications in a single region with networking and security services. 
article describes an automated approach for enterprises to establish environments for their programs and projects in a rapid, replicable manner using the principles of Infrastructure as Code (IaC). Key benefits of this approach are as follows:

    Accelerated time-to-value on cloud
    Standardization of deployment practices on cloud across the enterprise
    Rapid deployment of environments for projects
