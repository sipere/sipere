---
sidebar_position: 1
---

# Model generating

```bash
node op make:model <modelname> [options]
```

Options:

* -c, --controller Genarate controller file
* -m, --migration Generate migration file
* -s, --seeder Generate seeder file
* -t, --test Generate test file
* --modrel Generate modrels content
* -r, --router Generate router for api.js
* -a, --all Generate all files and content

## For example

The model name is written in lowercase, singular.

```bash
node op make:model employee -a
```
