# GboardWu prebuilt for LineageOS

Gboard 18.5.4.993608717 (arm64-v8a) with Gboard Patches v4.1,
package `dev.jason.com.google.android.inputmethod.latin`.

Installed as a regular (non-privileged) presigned app in `/product/app`,
so updates signed by the same key install over it.

## Usage

Place this repo at `vendor/gboard`, e.g. via `.repo/local_manifests`:

```xml
<project path="vendor/gboard" name="murikbmx/gboard" remote="github" revision="main" />
```

and inherit it from the device makefile:

```make
$(call inherit-product-if-exists, vendor/gboard/gboard.mk)
```

## Updating

Replace `prebuilts/GboardWu.apk` with a newer build signed by the same key.
