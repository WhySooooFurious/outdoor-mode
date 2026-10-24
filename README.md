# Outdoor mode (native port)

Native ROM integration of https://github.com/Android-Artisan/Outdoor-mode
without Xposed/LSPosed.

- outdoor_mode.mk - include from a device .mk: $(call inherit-product, vendor/whysoo/outdoor-mode/outdoor_mode.mk)
- Android.bp - platform-signed system app OutdoorMode (package com.artisan.outdoormode):
  Quick Settings tile that flips Settings.System "display_outdoor_mode" +
  long-press trampoline to Settings -> Display.
- The brightness effect comes from a small frameworks/base patch
  (DisplayBrightnessController watches the key and drives the display to its
  maximum backlight while it is set).

Original idea and app structure: (c) Android-Artisan (GPLv3).
