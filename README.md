<img width="1921" height="819" alt="封面图" src="https://github.com/user-attachments/assets/7932dca7-df09-4e04-9b9d-39cfa53db2e6" />


# Android TV Optimization: Turn Android TV into Apple TV with Aerial

> Originally published on [LIZHI.SHOP](https://lizhi.shop/en/articles/android-tv-desktop-aerial-install-guide?cid=53qvofdc&utm_source=lizhi-shop&utm_medium=github), where selected software is available

Default Android TV home screens are frequently cluttered with sponsored banners, film posters, and recommended streaming content. By replacing the default launcher with lightweight open source utilities, you can achieve an Apple TV-style interface with minimalist aesthetics across hardware from brands like Xiaomi, FFALCON, and Sony.

TL;DR: Deploy **Aerial** for a clean launcher, pair it with **CleanYourTV** for background debloating, and organize desktop clutter on macOS using **Bartender 7**.

Tool | What it does | Notes
--- | --- | ---
Aerial-TV | Replaces default Android TV home screen with clean app icons and aerial wallpapers | Supports Apple TV dynamic screensavers and mobile QR configuration
CleanYourTV | Trims system bloatware and background telemetry services | Targets vendor-specific packages and startup processes
Bartender 7 | Manages macOS menu bar items with automated hide and show rules | Keeps menu bar space organized on displays with camera notches

## Aerial-TV: Replacing the TV Home Screen

The **Aerial** project focuses primarily on **replacing the TV home screen** with streamlined **app icons** and high-definition **dynamic backgrounds**. It provides a **Chinese-language tutorial** and verified documentation across an assortment of televisions and set-top boxes. While it does not alter underlying display hardware or streaming decoding, it eliminates promotional visual noise.

Deploying the launcher using an Android TV model, such as a Xiaomi television, follows a straightforward process:

### 1. Enable ADB Debugging

Navigate to "Settings > About" and **tap repeatedly** on the "Product Model" entry to activate developer mode. Return to "Settings > Account & Security" and toggle on "**ADB debugging**" along with the permission to install apps from unknown sources. Retrieve the TV IP address under the connected network properties, keeping in mind that navigation labels vary slightly between manufacturers.

### 2. Run the Agent Installation Script

Confirm that the computer and television connect to the same local network subnet. Open a compatible terminal assistant and execute the following automated command set, ensuring the target IP placeholder is updated:

```bash

Please help me install the open source TV home screen Aerial on my TV and set it as the home screen that loads at startup.

TV IP: YOUR_TV_IP

Keep ADB always on: Yes

The installation instructions are here: https://aerial.qust.me/agent.md?utm_source=lizhi-shop

(If that doesn't open, use https://raw.githubusercontent.com/pengchujin/aerial-tv/main/site/agent.md?utm_source=lizhi-shop )

Please read the installation instructions in full before you start, then run the commands yourself on my computer—don't just tell me the steps. Remind me when something needs to be done on the TV.

Finally, following the "Acceptance" section in the instructions, paste the raw output of the commands below exactly as it is—don't just write "success":

- adb shell "cmd package resolve-activity --brief -a android.intent.action.MAIN -c android.intent.category.HOME" (the resolved home screen)
- adb shell settings get secure enabled_accessibility_services (whether app.orchard.tv/app.orchard.tv.guard.HomeGuardService is in there)
- adb shell "dumpsys window | grep mCurrentFocus" (after pressing the Home button)

If the installation fails, tell me directly which step it got stuck on.

```

### 3. Confirm Debugging Authorization

When the television displays the **ADB debugging authorization** dialog, choose "Always allow" to conclude setup. If the authorization prompt fails to trigger, try **exiting the TV settings** screen and returning to the stock home screen.

## Hands-on Experience and Setup Adjustments

Once configured, Aerial renders smooth aerial landscape video screensavers. Users can **scan a QR code with your phone** to reorder icons without relying entirely on directional remote clicks.

<img width="1448" height="1086" alt="图 7" src="https://github.com/user-attachments/assets/8e633afb-21f0-41de-b6a1-e79ce244ca7b" />


Long-pressing an app icon lets users set it to **launch at startup** or **hide the app**. On devices intended for family members, essential streaming software can **open directly at startup**, while complex settings utilities can remain out of sight.

Before initiating the replacement, check your hardware model, review repository documentation, and verify the procedure for reverting to the factory launcher. Source code is maintained in the [Aerial-TV repository](https://github.com/pengchujin/aerial-tv?utm_source=lizhi-shop).

## CleanYourTV: Debloating Preinstalled Services

While Aerial manages the presentation layer, **CleanYourTV** addresses operating system clutter by removing **preinstalled components** and background **ad services**. Combining both projects strips away unwanted background daemons and prevents native system packages from reclaiming default desktop priority. Project scripts are published in the [CleanYourTV repository](https://github.com/Gathin23/cleanyourtv?utm_source=lizhi-shop).

## Bartender 7: Tidy the macOS Menu Bar

Display clutter is not unique to living room televisions. On macOS, running utilities quickly crowds the top menu bar, where space remains constrained on MacBook displays with a camera notch. Built-in system options provide limited control over visibility.

[Bartender 7](https://lizhi.shop/products/bartender?cid=53qvofdc&utm_source=lizhi-shop&utm_medium=github) lets you **automatically hide or show** menu bar icons based on custom workflow rules, hotkeys, and conditional triggers. Cloud synchronization daemons, capture utilities, and translation tools can stay tucked away until actively required. LIZHI.SHOP is an authorized reseller, with PayPal and credit card payment and human support if activation goes wrong.

## Summary

> [!TIP]
> - Replace cluttered Android TV home screens with Aerial to obtain dynamic aerial backgrounds and responsive launcher icons.
> - Utilize CleanYourTV to strip background ad packages and vendor bloatware for a more responsive system.
> - Reclaim constrained menu bar space on macOS by applying automated visibility rules with Bartender 7.

## Credits

Written by the LIZHI.SHOP editorial team, first published on [LIZHI.SHOP](https://lizhi.shop/en/articles/android-tv-desktop-aerial-install-guide?cid=53qvofdc&utm_source=lizhi-shop&utm_medium=github) on 2026-10-26

## Reference

- [Bartender 7 license on LIZHI.SHOP](https://lizhi.shop/products/bartender?cid=53qvofdc&utm_source=lizhi-shop&utm_medium=github)
- [Aerial-TV on GitHub](https://github.com/pengchujin/aerial-tv?utm_source=lizhi-shop)
- [CleanYourTV on GitHub](https://github.com/Gathin23/cleanyourtv?utm_source=lizhi-shop)

