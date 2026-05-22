## E-commerce Access Integrations (Pro)

The Pro module can connect private podcast access to supported commerce and membership plugins.

Supported providers in the plugin code are:

- Easy Digital Downloads.
- MemberPress.
- Paid Memberships Pro.
- WooCommerce.

Only installed and active providers are shown in the private podcasting settings.

## What the integration does

An access integration links a private podcast to a product, membership, level, or other provider-specific object. The integration can then grant or revoke private podcast access based on events from that provider.

The exact object label depends on the active provider. For example, it may be a product, membership, or level.

## Configure access integration

1. Install and configure the commerce or membership plugin.
2. Create the product, membership, or level that should unlock the podcast.
3. Open the podcast in **Selfhost Podcasting**.
4. Set the podcast to **Private**.
5. In the private podcasting settings, choose the e-commerce provider if more than one is active.
6. Choose the linked object.
7. Save options.

## If no provider appears

The settings panel only shows supported providers that are installed and active. If none are active, the plugin displays a notice listing the supported plugins.

## If a saved provider becomes inactive

If a provider was previously saved but is now inactive, the settings keep the saved mapping and show an inactive notice. Reactivate that plugin to browse its objects again, or switch to another available provider.

## Manual access and automatic access

Manual subscriber token generation can still be used even when an e-commerce integration exists. This is useful for:

- Complimentary access.
- Support cases.
- Internal testing.
- Guests outside the commerce system.

Automatic access should be handled by the active provider integration.

## Troubleshooting

**No products or memberships are available**

Create a compatible product, membership, or level in the provider plugin, then reload the Selfhost settings.

**Access was not granted after purchase**

Check that the correct provider and object are selected, the provider plugin is active, and the purchase or membership status is one that the integration treats as active.

**A user still has access after cancellation**

Check the provider status, token table, and integration hooks. You can manually revoke a token while investigating.
