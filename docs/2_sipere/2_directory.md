---
sidebar_position: 2
---

# Directory structure

```text
my-project/
  |-app/
  |  |-controllers/
  |  |-database/
  |  |-middleware/
  |  |-models/
  |  |-routes/
  |  |-app.js
  |  `-index.js
  |-database/
  |  |-migrations/
  |  `-seeders/
  |-docs/
  |-test/
  |-.env
  |-.env.example
  |-.env.test
  |-database.sqlite
  |-nodemon.json
  |-op
  |-package.json
  `-README.md
```

* app/

The application is developed in the app library, following the MVC pattern. The view in our case is the routing.

* /app/controllers/ Location of the controllers.
* /app/database/ Location of the database connection.
* /app/middleware/ Location of the middleware.
* /app/models/ Location of the models.
* /app/routes/ Location of the routes.
* /app/app.js The server program.
* /app/index.js Entry point.

* /database/ Location of migration and seeder files.
* /database/migrations/ Location of migration files.
* /database/seeders/ Location of seeder files.

* /docs/ Location of the documentation.
* /test/ Location of the test files.

* .env Location of the environment variables.
* .env.example Location of the example environment variables.
* .env.test Location of the test environment variables.
* nodemon.json Nodemon configuration file.
* op CLI parser.
