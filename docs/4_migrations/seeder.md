---
sidebar_position: 2
---

# Migrations

## Generate seeder file

Generate new seeder file:

```bash
node op make:seeder <migration_name>
```

For example:

```bash
node op make:seeder employee
```

Pissible file name:

* 2025_12_13_112951_seed_employee.js

## Writer seeder

The migration file

```javascript
import db from '../../app/models/modrels.js';

async function up({context: QueryInterface}) {
  if(db.Employee) {
    await db.Employee.bulkCreate([
      
    ]);
  }else {
    await QueryInterface.bulkInsert('employees', [

    ]);
  }

}

async function down({context: QueryInterface}) {
  await QueryInterface.bulkDelete('employees');
}

export { up, down }
```

If there is a model and it is registered in the modrels.js file, then we can use the bulkCreate() function. It is recommended to use this. If there is no model, we can use the bulkInsert() function.

For example:

```javascript
    await db.Employee.bulkCreate([
      { name: 'John Doe' },
      { name: 'Jane Doe' }
    ]);
```

Complett file:

```javascript
import db from '../../app/models/modrels.js';

async function up({context: QueryInterface}) {
  if(db.Employee) {
    await db.Employee.bulkCreate([
      { name: 'John Doe' },
      { name: 'Jane Doe' }
    ]);
  }else {
    await QueryInterface.bulkInsert('employees', [

    ]);
  }

}

async function down({context: QueryInterface}) {
  await QueryInterface.bulkDelete('employees');
}

export { up, down }
```

## Run seeder

We can run all seeders at once or a specific seeder.

Run all:

```bash
node op db:seed
```

Run one seeder:

```bash
node op db:seed <seeder_filename>
```

```bash
node op db:seed 2025_12_13_112951_seed_employee.js
```

## Reset seeders

```bash
node op db:seed:reset
```

The reset will undo all seeders.

## Rollback seeder

Rollback undoes the last seeder.

```bash
node op db:seed:rollback
```
