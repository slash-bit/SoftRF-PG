---
layout: default
title: T1000E SenseCap Setup
---
<link rel="stylesheet" href="assets/css/style.css">

<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-2BLMJBJ0TN"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-2BLMJBJ0TN');

  function trackDownload(fileName) {
    gtag('event', 'download', {
      'event_category': 'File',
      'event_label': fileName
    });
  }
</script>

# So you have got yourself a new shiny T1000E SenseCap
...and you are wondering what to do with it and how to get it to work with SoftRF?  
You have come to the right place! Follow these instructions carefully.

*Please note, currently Bootloader Flasher only runs on PC. Not for Mac users yet, sorry.*

---

1. **Download the Bootloader Flasher utility**: Ensure you have the latest bootloader file for the T1000E SenseCap.

<a href="https://github.com/slash-bit/SoftRF-PG/blob/5db81d402305bba09452b6f20d2c40bc0ccb5ed8/software/utils/T1000E_Flash_Bootloader/bootloader_flasher.exe"
   class="btn btn-primary"
   onclick="trackDownload('Bootloader Flasher Utility')">
   Download Bootloader Flasher Utility
</a>

---

2. **Connect your T1000E SenseCap**: Use a USB cable to connect your device to your computer.

3. **Run the Bootloader Flasher utility**: Double click the downloaded `bootloader_flasher.exe`.

![Bootloader Flasher Utility Screenshot](/images/BootloaderFlasher_1.png)

If you like the work that I have been doing, you can  
[☕ Buy me a coffee](https://ko-fi.com/vladbelayev)

---

## Install the SoftRF firmware

<a href="https://github.com/slash-bit/SoftRF-PG/blob/master/software/firmware/binaries/nRF52-CARD/SoftRF-firmware-Card_T1000E-1.7-a827d2-VB007-prd.uf2"
   class="btn btn-primary"
   onclick="trackDownload('SoftRF Firmware T1000E')">
   Download the latest SoftRF firmware for T1000E SenseCap
</a>

1. With device powered off, connect the T1000E to your PC via USB.  
2. Press the button to power on.  
3. Enter DFU mode by pressing & holding the button, quickly connecting the charging cable **twice**.  
4. Copy the firmware `.uf2` file to the `T1000-E` drive.  

![Firmware Drag and Drop](/images/t1000e-drive.png)

---

[**SenseCap T1000E Card Operating Instructions**](https://github.com/slash-bit/SoftRF-PG/blob/master/documents/Documentation/SenseCap%20T1000E%20Card%20Operating%20Instructions.md) {: .btn .btn-primary } — Learn more about device features, beep codes, and usage tips.
