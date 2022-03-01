---
icon: question
label: FAQ
---

# Frequently Asked Questions :thinking_face:

## How do I properly hand-off a Vercel project to the client?

While not as easy as Netlify, what I prefer to do is:

1. Have the client create their own [Vercel account](https://vercel.com/signup)
2. At the time of writing, Github connections can only be connected to one Vercel account at a time, so have the client [create a Github account](https://github.com/join) if they don't already have one, and transfer the project repo to them
3. Delete the dev project from your own Vercel account (this is so the client can utilize the project name and domain you were using during dev)
4. You or the client can now connect their newly transferred Github repo to their own Vercel account!

## How can I see the bundle size of my website?

Simply run `npm run analyze` from the project folder. This will run a build of your site and automatically open the [Webpack Bundle Analyzer](https://github.com/webpack-contrib/webpack-bundle-analyzer) visuals for your site's build files.
