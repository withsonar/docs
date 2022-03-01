---
order: 50
title: 'Sanity'
---

# Sanity Set Up

General documentation about [Sanity](https://www.sanity.io/docs/getting-started).

## Sanity CLI

More information about [Sanity CLI](https://www.sanity.io/docs/getting-started-with-sanity-cli).

1. If you don't have [Sanity CLI](https://www.sanity.io/docs/getting-started-with-sanity-cli) installed, first run `npm install -g @sanity/cli` to install it globally.

## Initialise Sanity

2. In the `/studio` folder, type `npm install && sanity init`.

!!! Reconfigured the Sanity Studio
During Sanity's initialisation it will warn you, type `Y` and hit `enter` when you see the following message:

```sh
? The current folder contains a configured Sanity studio. Would you like to reconfigure it? (Y/n)
```

!!!

3. When it asks you what dataset configuration to use, go with the `default`.

4. Add **CORS Origins** to your newly created Sanity project (visit: [manage.sanity.io](https://manage.sanity.io) and go to Settings > API):

- Add your Studio URLs **_with_** credentials: `http://localhost:3333` and `[subdomain].sanity.studio`
- Add your front-end URLs **_without_** credentials: `http://localhost:3000` and `https://[subdomain].vercel.app`

!!!warning **Important**
For "singleton" documents, like settings sections, the schema uses a combination of `__experimental_actions` and the new [actions resolver](https://www.sanity.io/docs/document-actions). If you are using this outside of the official Sanity Starter, you will need to comment out the `__experimental_actions` line in "singleton" schemas to publish settings for the first time. This is because a singleton is still a document type, and one needs to exist first before it can be edited. Additionally, if you want to create additional "singleton" schemas, be sure to edit the `singletons` array in the following file: `/studio/parts/resolve-actions.js`.
!!!
