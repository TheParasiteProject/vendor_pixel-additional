# vendor_pixel-additional
Additional Pixel stuffs

## Note for Google Play system updates support
You need to set `TARGET_FLATTEN_APEX` to `false` in your device tree
<br>For example, in [PixelExperience](https://github.com/PixelExperience), you should add this flag to `aosp_(device-code-name).mk`

```TARGET_FLATTEN_APEX := false```

And then include the `config.mk`'s path to your device.mk

```$(call inherit-product-if-exists, vendor/pixel-additional/config.mk)```

Also, you can possible to build non-updatable flattened APEX too.
<br>Since [StatiXOS](https://github.com/StatiXOS)' [partner modules](https://git.statixos.com/sourajitk/vendor_partner_modules) supports it.
<br>For that, set `TARGET_FLATTEN_APEX` to `true` instead.

```TARGET_FLATTEN_APEX := true```

## Note for including CarrierSettings
You need to set `TARGET_INCLUDE_CARRIER_SETTINGS` to `true` in your device tree
<br>For example, in [PixelExperience](https://github.com/PixelExperience), you should add this flag to `aosp_(device-code-name).mk`

```TARGET_INCLUDE_CARRIER_SETTINGS := true```

And then include the `config.mk`'s path to your device.mk

```$(call inherit-product-if-exists, vendor/pixel-additional/config.mk)```

## Note for including additional GApps
This repo also includes several additional GApps packages, such as 
* `TARGET_INCLUDE_CAMERA_GO`: Camera from Google (Formerly, Camera Go or GCam Go)
* `TARGET_SUPPORTS_LILY_EXPERIENCE`: Enabling Android (Go Edition) device specific features
* `TARGET_INCLUDE_ADDITIONAL_GAPPS`: Additional GApps (Drive, Maps, Gmail, Tips)
