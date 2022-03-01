---
order: 45
title: 'Shopify'
---

# Shopify Set Up

General documentation about [Shopify](https://shopify.dev/api).

## Shopify Storefront Access

More information about [Shopify Storefront API](https://shopify.dev/api/storefront)

1. Enable Private Apps in Shopify
   - Apps > "Manage Private Apps" _(text link in page footer)_
   - Enable Private Apps
2. Create new Private App
   - Apps > Manage Private Apps > "Create private app"
   - Give this a relevant name, I prefer: "Headless Storefront", so it's clear what it's being used for
   - Use your dev email to know when there are issues
   - Change Admin API permissions on "Products" to `Read and write`
   - Allow this app to access your storefront data using the Storefront API, with at least the following permissions:
     - Read inventory of products and their variants
     - Read and modify checkouts

## Shopify Webhooks

1. Go to "Settings" _(bottom left)_ -> "Notifications" -> "Webhooks" _(very bottom)_
2. add the following webhooks:

- product creation - `[your-domain]/api/shopify/product-update`
- product update - `[your-domain]/api/shopify/product-update`
- product deletion - `[your-domain]/api/shopify/product-delete`

!!! Note
You have to use a real domain name (no localhost). Be sure to use your Vercel project URL during development, and then switch to the production domain once live. You may not know your Vercel project URL until you deploy, feel free to enter something temporary, but make sure to update this once deployed!
!!!

## Change `theme.liquid`

Since we're serving our store through a headless environment, we don't want visitors accessing our unused shopify theme. The domain for this is visible during checkout, and is publicly accessible. To silence it, replace your current theme's `theme.liquid` file with the one from this repo, and replace `YOUR_STOREFRONT_DOMAIN_NO_PROTOCOL` with your actual frontsite domain URL **(do not include protocol or trailing slash)**.

This will essentially "pass-through" URLs accessed at your Shopify Store to your true headless storefront _(ie. `shop.example.com/products` -> `example.com/products`)_
