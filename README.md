# Send-Browser-TV
Send Browser TV** is a **smartphone app (Android)** that lets you **download APKs directly from the built‑in browser** and then **send/install them on your TV / TV Stick over Wi‑Fi** using **ADB (TCP 5555)

<a href="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/177568106261bc.png" target="_blank">
  <img 
    src="https://raw.githubusercontent.com/ilblogdicristiangallo/Send-Browser-TV/main/ScreenShot/177568106261bc.png" 
    style="display: block; margin: 0 auto; width: 80%; max-width: 250px; border:1px solid #ccc; border-radius:8px; cursor:pointer;"
  >
</a>

It is **NOT** an app to install on the TV.  
You install **Send Browser TV on your phone**, download APKs on the phone, and push them to:

- **Android TV**
- **Google TV**
- **Amazon Fire TV / Fire TV Stick (Fire OS 5, 6, 7, 8)**

---

# What it does

1. You browse the web on your **phone** inside the app
2. You download an **APK**
3. You select your TV / Stick (Manual IP or Auto Scan)
4. The app connects via **ADB over network** and:
   - uploads the APK to the TV (`/data/local/tmp/`)
   - runs the install command (`pm install -r`)

The first time you connect, the TV may show an authorization popup like:
**“Allow USB debugging?”** → you must press **ALLOW** with the TV remote.

---

# Features

- Built‑in browser (GeckoView) to browse and download APKs
- Download progress (size, speed, ETA)
- Save downloads to:
  - App folder (default), or
  - Custom folder via Android SAF (Storage Access Framework)
- Send APK to TV over Wi‑Fi:
  - **Manual IP** (recommended)
  - **Auto Scan** local subnet for devices with port **5555** open
- ADB upload + install:
  - Push APK to `/data/local/tmp/`
  - Install using `pm install -r`

---

# Requirements

# Phone
- Android smartphone/tablet
- Connected to the **same Wi‑Fi network** as the TV/Stick

# TV / Stick
Your TV must accept ADB connections over the network.

# Fire TV / Fire TV Stick (Fire OS 5–8)
1. **Settings → My Fire TV → Developer options**
2. Enable:
   - **ADB debugging** = ON
   - (recommended) **Apps from Unknown Sources / Install unknown apps** = ON
3. When prompted on the TV, select **ALLOW**

# Android TV / Google TV
1. Enable Developer Options:
   - **Settings → System → About**
   - Press **Build** 7 times
2. Open **Developer options**
3. Enable:
   - **USB debugging / ADB debugging** = ON
   - **Network debugging / ADB over network (TCP 5555)** if available
4. When prompted on the TV, select **ALLOW**

> Some Android/Google TV devices (Android 11+) may use **Wireless debugging (pairing)** instead of TCP 5555.  
> Send Browser TV is designed for **ADB TCP 5555**.

---

# How to use

### 1) Download an APK (on your phone)
https://github.com/ilblogdicristiangallo/Send-Browser-TV/releases/download/apk%2Csend%2Cbrowser%2Ctv%2Csmart-tv%2Candroid%2Candroid-tv%2C/Send_Browser_TV-app-release.apk
1. Open **Send Browser TV**
2. Browse to a website and download an APK
3. Wait until the download completes

### 2) Send/Install on TV (over Wi‑Fi)
After the download:
1. Tap **Send APK to TV**
2. Choose a method:

#### Option A — Manual IP (Recommended)
1. Tap **Manual IP**
2. Enter the TV/Stick IP (example: `192.168.1.125`)
3. Tap **Test ADB Port (5555) & Install**
4. Look at the TV screen and press **ALLOW** if the popup appears

#### Option B — Auto Scan
1. Tap **Auto Scan (ADB 5555)**
2. Tap **Start Scan**
3. Select the detected device
4. Accept the ADB popup on the TV if shown

### No devices found (Auto Scan)
- Phone and TV must be on the **same Wi‑Fi**
- Enable **ADB debugging**
- Some routers block device‑to‑device traffic (AP isolation)

### “Cannot reach IP:5555” / “Connection refused”
- ADB over network is not enabled on the TV/Stick
- Wrong IP address
- Router/firewall blocks port 5555

### No ADB popup appears
- On the TV:
  - **Revoke USB debugging authorizations**
  - Toggle ADB debugging OFF/ON
- Try again from the app

### Install fails (unknown sources / permission)
- Enable **Install unknown apps / Unknown sources** on the TV/Stick

# Screen USE 

<table>
  <tr>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen1.jpeg?raw=true" width="200"></td>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen2.jpeg?raw=true" width="200"></td>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen3.jpeg?raw=true" width="200"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen4.jpeg?raw=true" width="200"></td>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen5.jpeg?raw=true" width="200"></td>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen6.jpeg?raw=true" width="200"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen7.jpeg?raw=true" width="200"></td>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen8.jpeg?raw=true" width="200"></td>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen9.jpeg?raw=true" width="200"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen10.jpeg?raw=true" width="200"></td>
    <td><img src="https://github.com/ilblogdicristiangallo/Send-Browser-TV/blob/main/ScreenShot/Screen11.jpeg?raw=true" width="200"></td>
    <td></td>
  </tr>
</table>
