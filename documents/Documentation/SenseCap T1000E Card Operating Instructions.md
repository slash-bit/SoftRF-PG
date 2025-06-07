# SenseCap T1000E Card Operating Instructions

When you first power on after the update, the card will start in its default configuration, operating in **FANET mode** with the aircraft type preset to **Paraglider**.  
A solid green LED indicates that the battery power is good and the device is **NOT airborne**.

---

### LED and Beep Indicators

#### Airborne Mode
<div style="display: flex; align-items: center; margin-bottom: 20px;">
    <img src="https://github.com/user-attachments/assets/805c77c1-5a17-4edd-8418-4d43c42f9316" alt="T1000E Slow Blink" width="150" style="margin-right: 10px;">
    <span><strong>Slow Blink</strong> - Indicates the device is in airborne mode.</span>
</div>

#### Battery Charge Status
After switching the device on, the battery charge status is indicated by a sequence of short beeps:

- **5x Beep**: Battery is charged 95% or more.  
- **4x Beep**: Battery is charged 75% or more.  
- **3x Beep**: Battery is charged 55% or more.  
- **2x Beep**: Battery is charged 35% or more.  
- **1x Beep**: Battery is charged 15% or more.  

If the battery is less than 15% charged, you will hear a constant beep for one second after switching the device on.  
A **LOW** battery charge level is also indicated by a rapidly flashing LED.

---

### Changing Settings on the Go

#### Protocol Mode
Double-click the button to toggle between **FANET** and **FLARM** modes. The device will reboot after the change.  
Confirmation tones will indicate the selected mode:
- **Two long tones**: FLARM mode.  
- **Two short tones**: FANET mode.  

<div style="display: flex; align-items: center; margin-bottom: 20px;">
    <img src="https://github.com/user-attachments/assets/e6e9bc11-863f-4a09-a5eb-e975481938e0" alt="T1000E Double click" width="250" style="margin-right: 10px;">
</div>

#### Buzzer Sound Volume
Single-click the button to cycle through the buzzer volume levels: **FULL > LOW > OFF**.  
- **FULL**: Two rising tones.  
- **LOW**: Two same-pitch tones.  
- **OFF**: Two lowering tones.  

---

### Changing Settings in the Settings File

Additional settings can be modified in the `settings.json` file. Follow these steps:

1. Connect the powered-on T1000E card to your PC/Mac.  
2. If connecting for the first time, you will be prompted to format the drive. Format it.  
3. After formatting, reconnect the device. A storage drive window will open.  
4. Double-click the button to initialize the settings file. This will write a file to the drive and reboot the device.  
5. Reconnect the device to your PC/Mac. A drive will appear with a `settings.json` file.  
6. Open the file in a text editor (e.g., Notepad). It will look like this:

```json
{
  "class": "SOFTRF",
  "protocol": "FANET",
  "band": "EU",
  "aircraft_type": "PARAGLIDER",
  "aircraft_id": "000000",
  "alarm": "DISTANCE",
  "txpower": "FULL",
  "volume": "FULL"
}
```

#### Field Explanations
- `"class"`: Always set to `"SOFTRF"`.  
- `"protocol"`: Options include `"FANET"`, `"LEGACY"`, `"ADS-L"`, `"OGNTP"` (OGN Tracking Protocol), `"P3I"` (PilotAware).  
- `"band"`: Region-specific options such as `"EU"`, `"US"`, `"AU"`, `"NZ"`, `"CN"`, etc.  
- `"aircraft_type"`: Options include `"PARAGLIDER"`, `"GLIDER"`, `"HANGGLIDER"`.  
- `"aircraft_id"`: Default is `"000000"`. You can set a 6-character hex ID.  
- `"alarm"`: `"DISTANCE"` for distance-based alerts or `"VECTOR"` for collision-course alerts.  
- `"txpower"`: Options are `"FULL"`, `"LOW"`, or `"OFF"`.  
- `"volume"`:  
  - `"FULL"`: Buzzes for any aircraft in proximity.  
  - `"LOW"`: Buzzes only for gliders, helicopters, or non-paraglider traffic.  
  - `"OFF"`: Disables the buzzer.  

After making changes, save the file and overwrite the existing one. A backup will be created as `settings_bac.json` in case you need to revert.

---

### Final Steps
After saving the changes, power off and power on the device to apply the new settings.
