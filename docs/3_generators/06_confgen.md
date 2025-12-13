---
sidebar_position: 6
---

# Configuration file

## Geneate .env file

```bash
node op conf:generate
```

The command generates the configuration file, named .env.

## Generate .env.test file

```bash
node op testconf:generate
```

This will create a file named .nev.test in the root directory of the project.

In the .env.test file, the database is set to be an in-memory database.
