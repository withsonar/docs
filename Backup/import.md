---
order: 45
title: 'Import Dataset'
icon: 'package-dependencies'
---

# Import

More information about the [Dataset](https://www.sanity.io/docs/dataset).

**EXPORT -> CREATE -> IMPORT** (more details [here](https://www.sanity.io/guides/multi-environment-deployments)).

```
sanity dataset export source-dataset-name source-dataset-name.tar.gz
sanity dataset create target-dataset-name --visibility public
sanity dataset import source-dataset-name.tar.gz target-dataset-name
```
