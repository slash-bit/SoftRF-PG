---
layout: default
title: T1000E SenseCap Setup
---

<link rel="stylesheet" href="assets/css/buttons.css">

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

1. **Download the Bootloader Flasher utility**: Ensure you have the latest bootloader file for the T1000E SenseCap called "bootloader_flasher.exe"

<a href="https://github.com/slash-bit/SoftRF-PG/releases/download/v1.0/bootloader_flasher.exe"
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

<a href="https://github.com/slash-bit/SoftRF-PG/releases/download/v007/SoftRF-firmware-Card_T1000E-1.7-a827d2-VB007-prd.uf2"
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

<style>
  #bmc-widget {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #FF813F;
    color: white;
    padding: 12px 18px;
    border-radius: 50px;
    font-weight: bold;
    font-size: 16px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    cursor: pointer;
    z-index: 1000;
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  #bmc-widget:hover {
    background: #e37428;
    text-decoration: none;
  }
  #bmc-widget svg {
    width: 24px;
    height: 24px;
  }
</style>

<a id="bmc-widget" href="https://ko-fi.com/vladbelayev" target="_blank" rel="noopener noreferrer">
  ☕ Buy me a coffee
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" 
       stroke-linecap="round" stroke-linejoin="round" class="feather feather-coffee">
    <path d="M18 8h1a4 4 0 0 1 0 8h-1"></path>
    <path d="M2 8h16v9a4 4 0 0 1-4 4H6a4 4 0 0 1-4-4z"></path>
    <line x1="6" y1="1" x2="6" y2="4"></line>
    <line x1="10" y1="1" x2="10" y2="4"></line>
    <line x1="14" y1="1" x2="14" y2="4"></line>
  </svg>
</a>
