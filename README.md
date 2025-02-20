# Activity Launcher for Android Security Testing
This Android app allows security testers to dynamically launch another app’s activity by providing a package name and activity name. It supports both ADB execution and manual input via UI, making it a useful tool for testing exported activities, deep link vulnerabilities, and inter-process communication security.

## Features
✔ Launch any app’s activity dynamically via ADB or UI input.<br/>
✔ Detect improperly exported activities that could be exploited.<br/>
✔ Bypass app entry restrictions by launching hidden or debug activities.<br/>
✔ Automate security testing using ADB shell commands.<br/>
✔ No root required, works on standard Android devices.<br/>

## Usage
### 1️⃣ Launch via ADB (Automated Testing)
`adb shell am start -n com.example.launcher/.MainActivity --es "package" "com.vulnerable.app" --es "activity" "com.vulnerable.app.HiddenActivity"`
If the activity launches without authentication, it may indicate a security risk.

### 2️⃣ Launch via UI (Manual Testing)
Open the app.<br/>
Enter the package name and activity name.<br/>
Tap Launch Activity.<br/>
If the target activity opens unexpectedly, investigate further.<br/>

## Security Testing Use Cases
✔ Identify unprotected exported activities in AndroidManifest.xml.<br/>
✔ Check if launching an activity bypasses authentication.<br/>
✔ Test for insecure intent handling and deep link vulnerabilities.<br/>
✔ Examine privilege escalation risks through improperly configured components.<br/>

## Disclaimer: 
This tool is intended for ethical security testing and research purposes only. Do not use it on apps without proper authorization. 🚀<br/>
