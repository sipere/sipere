---
sidebar_position: 2
---

# Using admin user

The users table has a roleId field. By default, it is set to 0. The isAdmin middleware checks the roleId field. It only allows a route to be used if the roleId value is 1.

Order is important! isAdmin must be preceded by verifyToken.

```javascript
import isAdmin from '../middleware/authAdmin.js';

//...

router.post('/products', [verifyToken, isAdmin], ProductController.store);
```
