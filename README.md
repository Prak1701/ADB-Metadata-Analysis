# Mobile & App Metadata Analysis using ADB

This project demonstrates how to use **Android Debug Bridge (ADB)** for basic device profiling, application metadata extraction, and system diagnostics.  
It was carried out as part of my academic project to gain **hands-on experience** with mobile forensics and testing tools.

---

## Project Objectives
- Learn how to connect and interact with an Android device via ADB.
- Extract **device-level information**: model, OS version, battery, storage, resolution, uptime.
- Perform **application metadata analysis**: installed packages, app versions, permissions, install/update times.
- Capture **visual evidence**: screenshots and screen recordings directly using ADB.
- Collect **system diagnostics**: running processes, logs, and app data usage.

---

## Tools & Setup
- **ADB (Android Debug Bridge)** – from Android SDK Platform Tools.
- **Windows CMD / PowerShell** for running commands.
- **Android Device** with USB Debugging enabled.

---

## Project Workflow
1. **Device Profiling**  
   - `adb devices` → verify connection.  
   - `adb shell getprop ro.product.marketname` → device model.  
   - `adb shell getprop ro.build.version.release` → Android version.  
   - `adb shell dumpsys battery` → battery details.  
   - `adb shell wm size` → screen resolution.  
   - `adb shell uptime` → uptime since last reboot.  
   - `adb shell df -h /` → storage usage.  

2. **App Metadata Analysis**  
   - `adb shell pm list packages` → list installed apps.  
   - `adb shell dumpsys package <packagename>` → metadata (version, install date, permissions).  

3. **System Diagnostics**  
   - `adb shell ps` → running processes.  
   - `adb logcat -d` → system logs.  
   - `adb shell du -h /sdcard/<AppFolder>` → app data usage.  

4. **Visual Evidence**  
   - `adb shell screencap -p /sdcard/screen.png` → screenshot.  
   - `adb shell screenrecord /sdcard/demo.mp4 --time-limit=10` → short video recording.  

---

## Evidence (Screenshots)
Some example outputs from my project (see `/evidence/` folder):
- Device connection (`adb devices`)
- Device model & version
- Battery status
- Screen resolution
- Uptime
- Storage usage
- Installed packages
- Running processes
- Logs
- Screenshot & Screen recording proof

---

## Key Learnings
- Gained practical exposure to **ADB commands** for mobile analysis.  
- Understood how metadata can be used in **testing and forensics**.  
- Learned how to capture and organize **evidence systematically**.    
