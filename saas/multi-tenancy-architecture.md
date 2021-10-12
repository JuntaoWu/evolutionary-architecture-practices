---
description: Design a multi-tenancy architecture to achieving SAAS
---

# Multi-tenancy Architecture

There are several approaches to choose when considering multi-tenancy architecture implementation.

1. Same runtime environment for multiple tenants.
2. One runtime environment for each tenant domain.
3. One resource container for each tenant domain.

These approaches are listed in an order of isolation level ascending. We can implement a hybrid approach where choose different options for different workload classes. For example, provide a shared runtime environment for multiple tenant domains to a set of tenants, and provide a runtime environment for each tenant domain to another set of tenants.

Refer to the concrete project we are developing. We deployed the application running across multi server environments currently. 

There are thousands organizations accessing our app. Each organization have around hundreds up to 3k persons. The system record person's basic information & salary information as an aggregate. Briefly speaking, there are 100k Business Entities across the system. 100k Domain Events produced per month. We have a target to support 2m Entities in total, and 2m Events / month. 

It's reasonable to achieve high availability & high concurrency via horizontal scale. 
