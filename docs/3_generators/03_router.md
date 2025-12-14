---
sidebar_position: 3
---

# Router generating

```bash
node op make:route <name>
```

The name must be an existing controller.

For example:

```bash
node op make:router employee
```

This command creates routing entries for all CRUD operations in the api.ts file. The router name is written in lowercase and singular.

Example:

```javascript
import EmployeeController from '../controllers/employeeController.js';
//...
router.get('/employees', EmployeeController.index);
router.get('/employees/:id', EmployeeController.show);
router.post('/employees', EmployeeController.store);
router.put('/employees/:id', EmployeeController.update);
router.delete('/employees/:id', EmployeeController.destroy);
```

You can edit the entered lines as needed.
