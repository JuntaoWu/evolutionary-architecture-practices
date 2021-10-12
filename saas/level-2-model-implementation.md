---
description: The way to achieve a configurable software
---

# Level 2 model implementation

`Level 2 - Configurable: This adds greater program flexibility through configurable metadata, so many customers use separate instances of the same application code. This lets the vendor meet different customer needs through detailed configuration options, while simplifying common code base maintenance and updating.`

The primary pattern is separation of configuration data from application code. Find the properties of your application that may vary among different tenants, and pull those properties out into a configuration system.

A centralized configuration contains below 3 levels of aspects:

#### System level 

Spring Cloud Config provides server-side and client-side support for externalized configuration in a distributed system. With the Config Server, you have a central place to manage external properties for applications across all environments. A running instance uses an application config.

#### Tenant level

Tenant stores settings such as organization settings / user settings as a whole when initializing or using the system daily. These configuration cannot be treated as system level because it could not be determined when the application start up.

#### Application level

Application level configuration refer to a traditional way how we implement a configurable product. There are several difference between tenant level config & application level config. 

* The specified target are different.
* Tenant configuration does not require a unique config set for a system, whereas the application configuration does.
* A tenant configuration could be maintained by the tenant administrator themselves, while an application configuration is maintained by the DevOps team.
* As we should provide the ability to use our application out-of-box, the tenant configuration should be a predefined application configuration already. A tenant cannot set settings unless such settings were provided.

As stated in Wikipedia, 

SaaS applications similarly support what is traditionally known as application [configuration](https://en.wikipedia.org/wiki/Computer_configuration). In other words, like traditional enterprise software, a single customer can alter the set of configuration options (a.k.a. [parameters](https://en.wikipedia.org/wiki/Parameter_\(computer_programming\))) that affect its functionality and [look-and-feel](https://en.wikipedia.org/wiki/Look-and-feel). Each customer may have its own settings (or: parameter values) for the configuration options. The application can be customized to the degree it was designed for based on a set of predefined configuration options.\[[citation needed](https://en.wikipedia.org/wiki/Wikipedia:Citation_needed)]

For example, to support customers' common need to change an application's look-and-feel so that the application appears to be having the customer's [brand](https://en.wikipedia.org/wiki/Brand) (or—if so desired—[co-branded](https://en.wikipedia.org/wiki/Co-branding)), many SaaS applications let customers provide (through a [self-service](https://en.wikipedia.org/wiki/Self-service) interface or by working with application provider staff) a custom logo and sometimes a set of custom colors. The customer cannot, however, change the [page layout](https://en.wikipedia.org/wiki/Page_layout) unless such an option was designed for.\[[citation needed](https://en.wikipedia.org/wiki/Wikipedia:Citation_needed)]

What we need to do is to implement a service to provide such manageable settings for application. Determine and Migrate the reconfigurable application configs to a user configurable manner.

