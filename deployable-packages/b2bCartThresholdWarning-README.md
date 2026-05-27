# B2B Cart Threshold Warning Deployment Package

This package contains the metadata needed to show the cart-page approval threshold warning before checkout starts.

## Contents

- `package.xml`
- `lwc/sDO_SCOM_OOA_CustomCheckout/*`
- `flows/SDO_B2BCommerce_Cirrus_Checkout_Enhanced.flow`

## Deploy From Directory

```sh
sf project deploy start --metadata-dir deployable-packages/b2bCartThresholdWarning
```

## Validate From Directory

```sh
sf project deploy start --metadata-dir deployable-packages/b2bCartThresholdWarning --dry-run
```

## Deploy From ZIP

```sh
sf project deploy start --metadata-dir deployable-packages/b2bCartThresholdWarning.zip --single-package
```

## Validate From ZIP

```sh
sf project deploy start --metadata-dir deployable-packages/b2bCartThresholdWarning.zip --single-package --dry-run
```

## Portability Notes

The target org must already have compatible B2B Commerce checkout metadata, including the `SDO_B2BCommerce_Cirrus_Checkout_Enhanced` flow and the cart page placement for `sDO_SCOM_OOA_CustomCheckout`.

This package intentionally does not include `dynamicHeroBanner` or the retired `SDO_B2BCommerce_Subflow_Cart_Validation_Threshold` flow.
