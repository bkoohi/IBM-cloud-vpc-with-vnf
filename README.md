# Securing Kubenetes workload in IBM Cloud VPC with Palo Alto. 

Container applications in IKS or ROKS in IBM Cloud VPC would need a full firewall security service that a production workload needs. Our client design objective might be not to expose their application directly to internet without a firewall protection. IBM Cloud provides network and security services such as VPC, ALBs and NFVs such as Palo Alto to meet these objectives.

The architecture in this design provides an automation for deploying mutltiple applications in a single region with networking and security services. 
article describes an automated approach for enterprises to establish environments for their programs and projects in a rapid, replicable manner using the principles of Infrastructure as Code (IaC). Key benefits of this approach are as follows:

    Accelerated time-to-value on cloud
    Standardization of deployment practices on cloud across the enterprise
    Rapid deployment of environments for projects
