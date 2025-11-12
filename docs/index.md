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

> **⚠️ Note:** Currently the Bootloader Flasher only runs on Windows PC. Not for Mac users yet, sorry.

---

## Step 1: Download Required Files

First, download both files you'll need for the complete setup:

### 1.1 Download Bootloader Flasher Utility

<a href="https://github.com/slash-bit/SoftRF-PG/releases/download/v1.0/bootloader_flasher_v2.exe"
   class="btn btn-primary"
   onclick="trackDownload('Bootloader Flasher Utility')">
   📥 Download Bootloader Flasher Utility
</a>

### 1.2 Download SoftRF Firmware

Download this now so it's ready when you need it in Step 3:

<a href="https://github.com/slash-bit/SoftRF-PG/releases/download/v007/SoftRF-firmware-Card_T1000E-1.7-a827d2-VB007-prd.uf2"
   class="btn btn-primary"
   onclick="trackDownload('SoftRF Firmware T1000E')">
   📥 Download SoftRF Firmware for T1000E
</a>

---

## Step 2: Flash the Bootloader

### 2.1 Connect Your Device
Use a USB cable to connect your T1000E SenseCap to your computer.

### 2.2 Run the Bootloader Flasher
Double-click the downloaded `bootloader_flasher.exe` file.

![Bootloader Flasher Utility Screenshot](/images/BootloaderFlasher_1.png)

### 2.3 Select COM Port and Flash
1. Select your device's COM port from the dropdown menu
2. Click the **"Flash Device"** button
3. Wait for the flashing process to complete

![Successful Flash Screenshot](/images/BootloaderFlasher_2.png)

> **✅ Success!** You should see a confirmation message when the bootloader is flashed successfully.

---

## Step 3: Install the SoftRF Firmware

After the bootloader flash completes successfully, a **File Explorer window will automatically pop up** showing the `T1000-E` drive.

### 3.1 Copy Firmware to Device
Simply **drag and drop** (or copy) the SoftRF firmware `.uf2` file you downloaded in Step 1.2 into the `T1000-E` drive window.

![Firmware Drag and Drop](/images/t1000e-drive.png)

> **💡 Tip:** If the File Explorer window doesn't appear automatically, you can manually enter DFU mode:
> 1. Power off the device
> 2. Press & hold the button
> 3. Quickly connect the USB cable **TWICE** (double-tap connection)
> 4. The `T1000-E` drive should appear

### 3.2 Complete Installation
Once you copy the firmware file, the device will automatically:
- Install the firmware
- Reboot
- Be ready to use with SoftRF!

---

## Additional Resources

[**📖 SenseCap T1000E Card Operating Instructions**](https://github.com/slash-bit/SoftRF-PG/blob/master/documents/Documentation/SenseCap%20T1000E%20Card%20Operating%20Instructions.md){: .btn .btn-secondary }

Learn more about device features, beep codes, and usage tips.

---

## Support This Project

If you found this tool helpful and would like to support continued development:

[☕ **Buy Me a Coffee**](https://ko-fi.com/vladbelayev){: .btn .btn-primary }

Your support helps maintain and improve these tools for the community. Thank you!

---

<style>
  /* Improved page styling */
  h2 {
    color: #2c3e50;
    border-bottom: 2px solid #3498db;
    padding-bottom: 10px;
    margin-top: 30px;
  }

  h3 {
    color: #34495e;
    margin-top: 20px;
  }

  blockquote {
    background-color: #f8f9fa;
    border-left: 4px solid #3498db;
    padding: 15px 20px;
    margin: 20px 0;
    border-radius: 4px;
  }

  blockquote p {
    margin: 0;
  }

  img {
    border: 1px solid #ddd;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    margin: 20px 0;
    max-width: 100%;
    height: auto;
  }

  .btn {
    display: inline-block;
    margin: 10px 5px;
    padding: 12px 24px;
    font-size: 16px;
    border-radius: 6px;
    text-decoration: none;
    transition: all 0.3s ease;
  }

  .btn-primary {
    background: #3498db;
    color: white;
  }

  .btn-primary:hover {
    background: #2980b9;
    text-decoration: none;
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(52, 152, 219, 0.4);
  }

  .btn-secondary {
    background: #95a5a6;
    color: white;
  }

  .btn-secondary:hover {
    background: #7f8c8d;
    text-decoration: none;
  }

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
    transform: translateY(-2px);
    box-shadow: 0 6px 15px rgba(0,0,0,0.4);
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
