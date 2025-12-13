---
sidebar_position: 4
---

# Modrel generating

Models are collected in the app/models/modrels.js file. The tables they represent can be linked here. The seeders also rely on this file.

```bash
node op make:modrel <model_name>
```

The name must be the name of an existing model.

For example:

```bash
node op make:modrel employee
```

The command registers the given model in the app/models/modrels.js file.

```javascript
import Employee from './employee.js';
//...
db.Employee = Employee;
```
