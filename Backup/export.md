---
order: 50
title: 'Export Dataset'
icon: 'package-dependents'
---

# Export

More information about the [Dataset](https://www.sanity.io/docs/dataset).

Export dataset to local filesystem as a gzipped tarball:

- `sanity dataset export production ./production.tar.gz`
- `sanity dataset export production ./production-$(date +%d-%m-%Y_%H-%M).tar.gz`

Copies a dataset including its assets to a new dataset:

- `sanity dataset copy source-dataset-name target-dataset-name`

!!! Note
It's important to note that `sanity dataset copy` doesn't work for the free tier.
!!!
