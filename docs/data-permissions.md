---
id: data-permissions
title: Data-permissions
---

## Data-permissions

We have two solutions for data permissions (filtering). Using implicit assignment APIs. Or just use BatchEnforce() API.

### How to query implicit roles or permissions?
When a user inherits a role or permission via RBAC hierarchy instead of directly assigning them in a policy rule, we call such type of assignment as ``implicit``.
To query such implicit relations, you need to use these 2 APIs: ``GetImplicitRolesForUser()`` and ``GetImplicitPermissionsForUser`` instead of ``GetRolesForUser()`` and ``GetPermissionsForUser``. For more details, please see [this GitHub issue](https://github.com/casbin/casbin/issues/137).

### `BatchEnforce()`

BatchEnforce enforces each request and returns result in a bool array

For example:

<!--DOCUSAURUS_CODE_TABS-->

<!--Go-->
```go
boolArray, err := e.BatchEnforce(requests)
```
<!--END_DOCUSAURUS_CODE_TABS-->
