---
order: 950
title: Features
icon: 'zap'
---

# Features

## Technologies

- Hybrid static & server rendering with [Next.js](https://nextjs.org/)
- Content management with [Sanity](https://www.sanity.io/) (unified content platform)
- Product (and variants) management powered by [Shopify Storefront API](https://shopify.dev/api/storefront)
- Checkout management powered by [Shopify Buy SDK](https://www.npmjs.com/package/shopify-buy)
- Real-time inventory check for products using [SWR](https://swr.vercel.app/) from [Vercel](https://vercel.com/)
- Utility-first CSS with [Tailwind CSS](https://tailwindcss.com/)
- Animations powered by [Framer Motion](https://www.framer.com/motion/)
- Automatic deployments with [Vercel](https://vercel.com/)
- Automatic preview URLs and A/B testing possibilities with [Vercel](https://vercel.com/)

## Functional

- Easy collaboration with Sanity built-in features
- Customizable Filtering & Sorting for product collections
- Dynamic Page Routes for custom page creation
- Automatic `Sitemap.xml` generation
- Automatic `robots.txt` generation
- Automatic 301 Redirects from Sanity
- Live Preview content directly from Sanity
- Modern Image component using Sanity's Hotspot, Crop, and automatic WEBP format
- Modular page content for all pages, including dynamic grid layouts
- Customizable Promotion Banner
- Customizable Cookie Notice

## Shopify Integration

- Automatically syncs products from Shopify into Sanity
- Custom action to sync product cart thumbnails back to Shopify from Sanity
- Tracks product status (draft/published) from Shopify to help control visibility while editing
- Deleted products and variants are preserved and flagged in Sanity
- Updates the URL on variant changes while keeping a clean history stack
- Vanity shop URL masking
- Global Cart with access to all variant data for line items
- Supports Single Variant products out of the box
- Product photo galleries with variant granularity
- Dynamic `/shop` collection page
- Custom collection pages
- Ability to surface a variant option on product cards

## APIs and External Services Integration

- [Klaviyo](https://www.klaviyo.com/) **waitlist** form for out-of-stock products
- [Klaviyo](https://www.klaviyo.com/) **newsletter** form with opt-in field
- [Google Tag Manager](https://tagmanager.google.com/) integration
- [ NOT DONE YET ] [Cloudinary](https://cloudinary.com/) integration

## Accessibility

- ARIA Landmark Roles
- Default focus states preserved for keyboard navigation
- Correctly trap focus for drawers with focus-trap-react
- Roving tabindex for radio buttons
- Input-based quantity counters
- Required `alt` text for all images
- "Skip to Content" link

## SEO Features

- Page-level SEO/Share settings with previews
- Fallback Global SEO/Share settings
- Automatic JSON-LD Schema markup for products

## Others

- High scores in Lighthouse
- Fully documented (installation, migration, improvement, deployment)
- Theme/website customisation made easy with Sanity (in the Settings)
- Multiple environments (development, production)
- Automatic data backup
- Possibility to create script to migrate data faster via Sanity mutations
