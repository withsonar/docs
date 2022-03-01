---
icon: tools
label: Troubleshooting
---

# Troubleshooting

## Error: Failed to communicate with the Sanity API

If you get this error in your CLI, you need to logout and log back in again. Simply do `sanity logout` and then `sanity login` to fix.

## Access your "product_sync" metafields in Shopify without using a plugin

Simply navigate directly to: `https://[store_id].myshopify.com/admin/bulk?resource_name=Product&edit=metafields.sanity.product_sync`

_(making sure to replace `[store_id]` with your Shopify Store ID)_
