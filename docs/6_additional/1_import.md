---
sidebar_position: 1
---

# Data import

It is possible to import the contents of CSV and JSON files.

Syntactic:

```bash
node op db:import <model> <filePath> [sep]
```

When importing, the file extension determines whether to try to interpret the content as a JSON or CSV file. The extensions that can be used are:

* .csv
* .json

## JSON példa

```json
[
  {
    "id": 1,
    "name": "John Doe"
  },
  {
    "id": 2,
    "name": "Jane Doe"
  }
]
```

The model name is in lowercase, as seen in the sample:

```bash
node op db:import employee employee_data.json
```

## CSV example

The CSV file must contain the field names.

```csv
id,name
1,John Doe
2,Jane Doe
```

The model name is in lowercase, as seen in the sample:

```bash
node op db:import employee employee_data.csv ","
```

The last parameter is the separator in the CSV file.
