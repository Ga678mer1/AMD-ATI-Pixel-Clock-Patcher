# Atikmdag Patcher (AMD/ATI Pixel Clock Patcher)
![image](https://user-images.githubusercontent.com/98732955/212462154-150a9698-fee0-40d0-bb49-dd2211bda970.png)

AMD/ATI Pixel Clock Patcher modifies the AMD/ATI video driver to allow higher resolutions and refresh rates by removing the 165 MHz pixel clock limit for single-link DVI and HDMI, the 330 MHz limit for dual-link DVI, and the 400 MHz limit for VGA.

- [ ] [Download Atikmdag Patcher for Windows/Linux](https://github.com/Ga678mer1/AMD-ATI-Pixel-Clock-Patcher/releases/download/atikmdag-windows/AMD.ATI.Pixel.Clock.Patcher.rar)

## Requirements:
+ Windows Vista or later
+ 5000-series GPU or newer
+ CrossFire: R9 280/280X and older cards require two CrossFire bridges if the pixel clock is greater than 300 MHz. This is only possible with cards that have two connectors. It will not work properly with more than two cards. Dual-GPU cards such as the 7990 will not work properly at higher pixel clocks.

## Compatibility:
+ Version 1.4.14 is compatible with Catalyst 11.9 to Adrenalin 22.10.1. It can be used with future versions if it finds the limits you need.
+ Riot Vanguard and FACEIT Anti-Cheat will not allow patched drivers to load.

## Getting started:
1. Run atikmdag-patcher.exe. (If you only need the BIOS signature patch, rename it to atikmdag-patcher-bios.exe first.)
2. If all limits are found, click "Yes" to patch and sign. If a limit is not found or if multiple matches are found, the patcher needs to be updated.
3. Reboot.

You can then add higher refresh rates using [Custom Resolution Utility (CRU)](https://www.monitortests.com/forum/Thread-Custom-Resolution-Utility-CRU).

To restore the unpatched driver, run the patcher again and click "Yes" to restore from backup.

Unpatching is not required before upgrading drivers. Simply run the patcher again after installing the new driver.

## Options:
+ You can rename the .exe file to change certain options:
+ atikmdag-patcher-bios.exe - Patch BIOS signature check only.
+ atikmdag-patcher-sl.exe - Make dual-link DVI ports act as single-link DVI. Use this to go beyond 230 MHz pixel clock with single-link DVI monitors.
+ atikmdag-patcher-dl.exe - Do not patch single-link DVI limit on dual-link DVI ports. Useful for 2560x1080 monitors.
+ atikmdag-patcher-self.exe - Use self-signed certificate. Windows test mode is required: https://www.monitortests.com/testmode.zip

## Known issues:

Legacy drivers may have issues with HDCP and video acceleration with the patch. Workarounds for video playback issues:
+ Disable hardware acceleration in the Flash Player settings (right-click on any Flash video and click "Settings...").
+ Use the Codec Tweak Tool to disable DXVA hardware acceleration under "Various Tweaks" (in the "Miscellaneous" section).

Older cards require the "LCD standard" vertical blanking/total to reduce the memory clock when idle. Horizontal values can still be reduced if necessary. Newer cards can handle some lower values depending on the resolution and refresh rate.

Older cards have a design limitation unrelated to the patch that causes video acceleration to scramble the screen if the vertical blanking/total is below standard with the video card's memory overclocked or with multiple monitors connected. Skype is known to trigger this problem. Either don't overclock the video card's memory, or use the "LCD standard" vertical blanking/total in CRU.

## Recent changes:
+ 1.4.14: Fix driver not found after installing Amernime Zone drivers. Added self-sign option and Info.txt. No changes to current drivers.
+ 1.4.13: Fixed low-resolution limit and restore from backup for very old drivers (11.9-12.4). No changes to later drivers.
+ 1.4.12: Updated for 21.9.1/21.9.2. Fixed CrossFire limit.
+ 1.4.11: Updated for 21.6.1-21.7.2. Fixed Radeon Software issues.
+ 1.4.10: Updated for 21.4.1.
+ 1.4.9: Fixed HDMI-DVI limit for 20.11.2 and HBlank limit for 20.5.1.
+ 1.4.8: Updated for 20.5.1.
+ 1.4.7: Find new SL-DVI/HDMI limit.
+ 1.4.6: Find new HDMI-DVI limit.
+ 1.4.5: Updated for 17.4.1. Find new DP-DVI/HDMI limit.
+ 1.4.4: Find BIOS signature check.
+ 1.4.3: Fixed HBlank limit for 16.12.1.
+ 1.4.2: Find 56 horizontal blanking (HBlank) limit.
+ 1.4.1: Fixed an issue that prevented the driver from loading correctly with earlier versions of Windows 10. This does not affect the anniversary update.
+ 1.4.0: Updated for 16.9.1. Changed the way the driver is located and patched. Replaced 640x480 limit with low-resolution limit. Fixed VGA limit for 32-bit.
+ 1.3.6: Find 10-resolution limit for Radeon Settings.
+ 1.3.5: Updated for 15.11 Crimson. Find 640x480 limit for Radeon Settings.
+ 1.3.4: Try to improve finding DVI/HDMI limit for newer drivers. Removed blue screen workaround for 14.6/14.7.
+ 1.3.3: Updated for 15.3. Fixed DVI/HDMI limit for 32-bit.
+ 1.3.2: Updated for 15.2. Fixed DVI/HDMI limit for 64-bit.
+ 1.3.1: Find 297 MHz HDMI 1.3+ limits. Run 3 times to properly repatch an existing installation.
+ 1.3: Removed blue screen workaround for 14.9. Fall back to self-signing if signing fails.
+ 1.2.7: Attempt to work around some antivirus false positives. Repatching is not necessary.
+ 1.2.6: Fixed AMD APP encoding for 14.6.
+ 1.2.5: Updated for 14.6. Fixed TMDS and VGA limits. Implemented workaround for SYSTEM_SERVICE_EXCEPTION blue screens.
+ 1.2.4: Updated for 14.4. Fixed SL limit on DL-DVI.
+ 1.2.3: Updated for 13.30 and upcoming 14.x releases.
+ 1.2.2: Find new HDMI limit for 12.9+.
+ 1.2.1: Find 400 MHz VGA limit.
+ 1.2: Test mode no longer required.

A message from ToastyX:
-----------------------
Over the years, I have created various monitor-related software and provided support for free. I would like to continue providing updates and work on new ideas, but I need your support. If you find my software useful, please consider supporting me through Patreon: https://www.patreon.com/ToastyX

![image](https://user-images.githubusercontent.com/98732955/212462280-b296e91f-f15f-4a7a-ab77-044d7876bc7d.png)

