---
description: A nestjs example for cqrs
---

# CQRS via Nestjs

A typical "resource" in nestjs is like this:

```
.
├── app.module.ts
├── main.ts
├── person-snapshot
│   ├── dto
│   │   ├── create-person-snapshot.dto.ts
│   │   └── update-person-snapshot.dto.ts
│   ├── entities
│   │   └── person-snapshot.entity.ts
│   ├── person-snapshot.controller.spec.ts
│   ├── person-snapshot.controller.ts
│   ├── person-snapshot.module.ts
│   ├── person-snapshot.service.spec.ts
│   └── person-snapshot.service.ts
```

Note the keyword resource is borrowed from the concept "REST" style, which means person-snapshot is a resource we can having GET/POST/PUT/PATCH/DELETE operations on it.

The flow of simple [CRUD](https://en.wikipedia.org/wiki/Create,\_read,\_update_and_delete) (Create, Read, Update and Delete) applications can be described using the following steps:

1. The **controllers** layer handles HTTP requests and delegates tasks to the services layer.
2. The **services layer** is where most of the business logic lives.
3. Services use **repositories / DAOs** to change / persist entities.
4. Entities act as containers for the values, with setters and getters.

 When our requirements become more complex, the **CQRS** model may be more appropriate and scalable.

