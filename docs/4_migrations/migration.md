---
sidebar_position: 1
---

# Migrations

## Generate migration file

Generate new migrations file:

```bash
node op make:migration <migration_name>
```

For example:

```bash
node op make:migration employee
```

Pissible file name:

* 2025_12_13_112951_create_employee.js

## Writer migration

The migration file

```javascript
import { DataTypes } from 'sequelize';

async function up({context: QueryInterface}) {
  await QueryInterface.createTable('employees', {
    id: {
      allowNull: false,
      autoIncrement: true,
      primaryKey: true,
      type: DataTypes.INTEGER
    },
    name: {
      type: DataTypes.STRING
    },
    createdAt: { type: DataTypes.DATE },
    updatedAt: { type: DataTypes.DATE }    
  });
}

async function down({context: QueryInterface}) {
  await QueryInterface.dropTable('employees');
}

export { up, down }
```

## Run migration

We can run all migrations at once, or a specific migration.

Run all migrations:

```bash
node op migrate
```

Run a single migration:

```bash
node op migrate <migration_filename>
```

For example:

```bash
node op migrate 2025_12_13_112951_create_employee.js
```

## Reset migration

```bash
node op migrate:reset
```

The reset will undo all migrations.

## Rollback migration

```bash
node op migrate:rollback
```

Rollback undoes the last migration.

## Fresh migration

```bash
node op migrate:fresh
```

Fresh undoes all migrations and then redoes all migrations.
