---
sidebar_position: 3
---

# Using different roles

We need to set the value 0, 1 or 2 in the roleId field of the users table. This way we already have three roles.

* 0 user
* 1 admin
* 2 superAdmin

The checkRole() middleware checks this.

The order is important! checkRole must be preceded by verifyToken.

```javascript
import checkRole from '../middleware/checkRole.js';

//...

router.post('/products', [verifyToken, checkRole(2)], ProductController.store);
```
