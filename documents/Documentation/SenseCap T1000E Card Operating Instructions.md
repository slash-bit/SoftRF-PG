# SenseCap T1000E Card Operating Instructions

When you first power on the device, the LED will be solid green 
which indicates that the battery power is good and the device is **NOT airborne**.
The device will beep according to the battery charge level (see below). After battery beeps you will hear Operating Mode indication beeps.

---

### LED and Beep Indicators



#### Battery Charge Status
After switching the device on, the battery charge status is indicated by a sequence of short beeps:

- **5x Beep**: Battery is charged 95% or more.  
- **4x Beep**: Battery is charged 75% or more.  
- **3x Beep**: Battery is charged 55% or more.  
- **2x Beep**: Battery is charged 35% or more.  
- **1x Beep**: Battery is charged 15% or more.  

If the battery is less than 15% charged, you will hear a constant beep for one second after switching the device on.  
A **LOW** battery charge level is also indicated by a rapidly flashing LED.

#### Radio Mode

This device suports three protocols LEGACY (FLARM), FANET and ADS-L. The selected protocol is indicated by the following beep sequences after the battery charge beeps:
- **Two long tones: FLARM mode.**
- **Two short tones: FANET mode.**
- **One longer tone: ADS-L mode.**

#### When Airborne
<div style="display: flex; align-items: center; margin-bottom: 20px;">
    <img src="https://github.com/user-attachments/assets/805c77c1-5a17-4edd-8418-4d43c42f9316" alt="T1000E Slow Blink" width="150" style="margin-right: 10px;">
    <span><strong>Slow Blink</strong> - Indicates the device is in airborne mode.</span>
</div>

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
  "aircraft_id": "4E3D2A",
  "alarm": "VECTOR",
  "alarm_filter": "PG",
  "txpower": "FULL",
  "volume": "FULL",
  "ignore_id": "201077",
  "sw_version": "SoftRF-1.7-VB007-prod"
}
```

#### Field Explanations
- `"class"`: Always set to `"SOFTRF"`.  
- `"protocol"`: Options include `"FANET"`, `"LEGACY"`, `"ADS-L"`, `"OGNTP"` (OGN Tracking Protocol), `"P3I"` (PilotAware).  
- `"band"`: Region-specific options such as `"EU"`, `"US"`, `"AU"`, `"NZ"`, `"CN"`, etc.  
- `"aircraft_type"`: Options include `"PARAGLIDER"`, `"GLIDER"`, `"HANGGLIDER"`.  
- `"aircraft_id"`: Default is `"000000"`. You can set a 6-character hex ID.  
- `"alarm"`: `"DISTANCE"` for distance-based alerts or `"VECTOR"` for collision-course alerts.
- `"alarm_filter"`: `"PG"` to filter alarms for paragliders. Or `"NONE"` for no filtering.
- `"txpower"`: Options are `"FULL"`, `"LOW"`, or `"OFF"`.  
- `"volume"`:  
  - `"FULL"`: High volume.  
  - `"LOW"`: Lower volume.  
  - `"OFF"`: Disables the buzzer.
- `"ignore_id"`: Default is `"000000"`. You can set a 6-character hex ID to ignore specific device, For exmple if you have two devices running side by side
- `"sw_version"`: Currently installed firmware version. Do not change this value.

After making changes, save the file and overwrite the existing one. Now, power off the SenseCap device by long pressing the button.  And then power it back on to apply the new settings.

---

### Registering you ID with databases
Use you aircraft ID generated in the settings file to register your aircraft ID with OGN or Puretrac databases, visit the following links:
- [OGN Registration](https://ddb.glidernet.org/)
- [Puretrack Registration](https://puretrack.io/)


