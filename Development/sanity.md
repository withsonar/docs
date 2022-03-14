---
order: 45
title: 'Sanity'
---

# Sanity

After following all the set up section, you can type `sanity start` in the `/studio` folder to start the studio locally.

Your Sanity Studio should be running on [http://localhost:3333](http://localhost:3333).

!!! Note
If you did not manually set up your project, the `projectId` in `/studio/sanity.json` will still be set to the demo project. Make sure to update this before starting the studio, otherwise you will be denied access when trying to access your studio.
!!!

## Setup a staging dataset

### Start by exporting/copying your production dataset

You likely already have a dataset named `production`, lets create a new one named `staging` and import the data from your production database to your staging database.

```
# Inside your SANITY studio folder
# Follow prompts to create a new dataset

sanity dataset create

# Export your production database

sanity dataset export

# Import your dataset into the staging environment

sanity dataset import production.tar.gz staging
```

### Setup the spaces API

Here is an example of the code you would need to add to your `sanity.json` config file to activate the spaces feature.

```json
// In your sanity.json file add
"__experimental_spaces": [
  {
    "name": "production",
    "title": "Production",
    "default": true,
    "api": {
      "projectId": "abcd1234", // replace with your projectId
      "dataset": "production"
    }
  },
  {
    "name": "staging",
    "title": "Staging",
    "api": {
      "projectId": "abcd1234", // replace with your projectId
      "dataset": "staging"
    }
  }
],
```

Restart your SANITY studio and you should now see a dropdown menu to switch between datasets in the top menu bar.

More information:

[!ref target="blank" text="Multi-environment deployments"](https://www.sanity.io/guides/multi-environment-deployments)
[!ref target="blank" text="How to setup a staging website with SANITY"](https://www.erichowey.dev/writing/how-to-setup-a-staging-website-with-SANITY/)
