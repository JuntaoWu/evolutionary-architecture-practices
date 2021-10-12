---
description: The 4 level SaaS Architecture Maturity Model by Microsoft
---

# SaaS Maturity Model

Microsoft’s SaaS maturity model provides a framework for accessing SaaS solutions and describing their maturity along three dimensions: scalability, multi-tenancy and configurability.

The SaaS maturity model is broken down into four levels, and each of them brings certain opportunities and challenges you should be aware of when accessing SaaS vendors.

 **Level 1 (Single-Tenant, Custom Instances)**

`At this level of the SaaS maturity model, the only way to support multiple customers (tenants) is to provide each of them a separate copy of the software. Because the provided copies can be customized by writing custom code, each customer is required to run a different instance of the software and scalability is non-existent, even though the software is technically delivered as a service. As such, no economies of scale can be harnessed, making this level the least cost-effective and sustainable when managing a larger number of customers.`

 **Level 2 (Single-Tenant, Configurable Instances)**

`At level 2, software can be customized by changing its configuration instead of writing custom code. In other words, all tenants interact with the same code configured in different ways, with each tenant running their own copy on a separate virtual or physical machine. Consequently, scalability and multi-tenancy are still not achieved. What’s more, the provider is at a competitive disadvantage because individual instances don’t share the same pool of computing power, which would make it possible to achieve economy of scale.`

 **Level 3 (Multi-Tenant, Configurable)**

`The third level of the SaaS maturity model can be described as being almost the perfect case because it includes both configurability and multi-tenancy, allowing each tenant to quickly and efficiently customize the same shared instance through a self-service tool. The only thing missing is scalability because software can be scaled up only by moving it to a more powerful server, which isn’t cost-effective. Still, the inefficient need for server space to accommodate many instances is eliminated and costs can be greatly reduced compared with level 2 of the SaaS maturity model.`

 **Level 4 (Multi-Tenant Configurable & Scalable)**

`Level 4 is the highest level of the SaaS maturity model. It combines the configurability and multi-tenancy of level 3 with scalability, making it possible to transparently add new software instances to the dynamic pool of instances with the help of a load balancer, whose job is to maximize the utilization of storage, processing power and other resources. Each tenant’s data is stored separately, and a virtually infinite number of tenants can be seamlessly accommodated by adjusting the number of servers on the backend to meet the current demand.`

As per spoken, we defined each deployment as a standard software version. So each customization for different area will be managed in a customized instance, a customized software version. We design this kind of SaaS first, and then achieve a more mature architecture model as fast as we can.

Why? Let's say we have 20 deployments right now. We'll have to make 20 different tests & deployments for a single Critical S1 issue hotfix as the code base and deployment package is different. So the earlier we can move to Level 2 model, the less risk we'll have in a long term maintainable point of view.

