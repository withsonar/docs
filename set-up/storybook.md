---
order: 30
title: 'Storybook'
---

# Storybook

General documentation about [Storybook](https://storybook.js.org/blog/get-started-with-storybook-and-next-js/).

## Install Packages

1. Inside the `studio` folder, install the Storybook Sanity plugin `npm i --save @sanity/storybook`

## Add the plugin into the `sanity.json`

Go to the `sanity.json` file and add the Storybook Sanity plugin into the `plugins` list.

```json
// ...
"plugins": [
    // ...
    "@sanity/storybook",
    // ...
  ],
  "env": {
    "development": {
      "plugins": ["@sanity/vision"] // or here, if you want to only have it in dev mode
    }
  },
// ...
```

!!! Note
You might have to change the Storybook port (e.g. from `9001` to `6006`).
Go to `/studio/config/@sanity/storybook.json` to change the value there.
!!!

## Import shared, global stylesheets in preview.js

```js
// .storybook/preview.js
import '../styles/tailwind.css';
import '../styles/app.css';
```

## Serve the public directory in Storybook

```js
// .storybook/main.js
module.exports = {
  staticDirs: ['../public'], // add this line
  // ...
};
```

## De-optimize Next.js Image in stories

!!!warning
More information about that [here](https://storybook.js.org/blog/get-started-with-storybook-and-next-js/).
!!!
