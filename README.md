# Lid Awake

Lid Awake keeps your laptop running with the lid closed, on a MacBook or a Windows laptop, and lets you use it from your phone (iPhone or Android): see how it's doing, watch and control its screen, and turn it on or off from anywhere. Everything goes over your own private Tailscale connection, so only you can reach it.

**Download:** [LidAwake-Mac.pkg](https://github.com/EdenHeiser/lid-awake-releases/releases/latest/download/LidAwake-Mac.pkg) for a Mac · [LidAwake-Windows.zip](https://github.com/EdenHeiser/lid-awake-releases/releases/latest/download/LidAwake-Windows.zip) for Windows · [all versions](https://github.com/EdenHeiser/lid-awake-releases/releases)

---

## 1. Install Tailscale on the laptop and your phone

Tailscale is a free app that makes a private, encrypted connection between your own devices.

- **Mac:** [tailscale.com/download/mac](https://tailscale.com/download/mac) · **Windows:** [tailscale.com/download/windows](https://tailscale.com/download/windows) · **iPhone:** App Store · **Android:** Google Play
- Sign in with **the same account** on the laptop and the phone. On the phone, allow the VPN when asked.
- Once for your account: open [login.tailscale.com/admin/dns](https://login.tailscale.com/admin/dns), make sure **MagicDNS** is on, and under **HTTPS Certificates** click **Enable**. (Forgot? The setup window reminds you.)

## 2. Install Lid Awake

### On a Mac (macOS 14 Sonoma or newer)

1. Download **[LidAwake-Mac.pkg](https://github.com/EdenHeiser/lid-awake-releases/releases/latest/download/LidAwake-Mac.pkg)** and double-click it in **Downloads**.
2. If macOS says it *can't check it for malicious software* or that Apple *could not verify* it, click **Done** (or **OK**). Then open **System Settings → Privacy & Security**, scroll down, and click **Open Anyway** next to "LidAwake-Mac.pkg". Type your Mac password if asked, and click **Open Anyway** again.
   *This happens once, because Lid Awake isn't registered with Apple yet.*
3. Click **Continue** → **Install**, and type your Mac login password.
4. Click **Close**. A **cup icon** appears in the menu bar at the top of the screen.

### On a Windows laptop

1. Download **[LidAwake-Windows.zip](https://github.com/EdenHeiser/lid-awake-releases/releases/latest/download/LidAwake-Windows.zip)** and unpack the **whole** ZIP (right-click it → **Extract All**).
2. Double-click **Install Lid Awake (Windows)**.
   - If Windows says **"Windows protected your PC"**, click **More info** → **Run anyway**.
   - If it asks **"Do you want to run this file?"**, click **Run**.
3. If a line shows **[X]**, it tells you what to do. Do it, then open the installer again.

## 3. Finish on the laptop

The **Set up Lid Awake** window opens by itself. (Later: on a Mac, click the cup → **Set up phone…**; on Windows, right-click the Lid Awake icon by the clock → **Set up phone…**.)

1. Fix anything it lists as missing (each line has a button).
2. **Phone password:** type a password (at least 10 characters) twice and click **Save password**.
3. Click **Turn Lid Awake on**. A **QR code** appears.

## 4. Add it to your phone

Make sure Tailscale is on on the phone.

- **iPhone:** point the **Camera** at the QR code and tap the link (it opens in Safari) → **Share** → **Add to Home Screen** → **Add**.
- **Android (Samsung or similar):** point the **Camera** at the QR code and tap the link → browser menu (**⋮** in Chrome, **≡** in Samsung Internet) → **Add to Home screen** (or **Install app**).

Open **Lid Awake** from the Home screen and type the phone password. In the app, the gear ⚙︎ turns on **Face ID** or **fingerprint** sign-in, and **Alerts**.

**To see and control the screen from the phone (Mac):** in the setup window click **Allow screen from phone**, then turn on **Lid Awake** in **Screen Recording** and in **Accessibility** (the window has a button for each).

---

## Every day

- **Turn it on:** click the cup (Mac) or the tray icon (Windows) and flip the switch, or use the phone.
- **For a while only:** choose **Turn off after** in the same menu.
- **Close the lid:** while Lid Awake is on, the laptop keeps running.
- It turns itself off if the battery gets low or too warm. Let it charge if you leave it running for long.

## Update

Download the new file above and install it the same way. Your password, settings and phone stay as they are.

Coming from Mac version 2.0.1 or older? macOS asks once more for **Screen Recording** and **Accessibility**: the setup window shows the buttons.

## Remove it

- **Mac:** open **Terminal** and run `sh ~/Applications/"Lid Awake.app"/Contents/Resources/uninstall.sh`. It asks whether to delete your settings too.
- **Windows:** double-click **Uninstall Lid Awake (Windows)** in the unpacked folder.

## Claude alerts (optional, for Claude Code users)

Your phone can show your Claude usage after each reply and alert you when Claude finishes or needs you.

- **Mac:** in **Terminal**, run `python3 ~/Applications/"Lid Awake.app"/Contents/Resources/tools/claude/setup.py on` (`off` turns it off).
- **Windows:** the installer asks; later, use the tray menu.
