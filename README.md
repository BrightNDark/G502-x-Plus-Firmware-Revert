# Logitech Mouse Firmware Rollback / Recovery

This repository contains a firmware rollback package that was provided directly to me by Logitech Support after a firmware update caused severe tracking issues with my mouse.

I am making the package available here for other users who may be experiencing the same problem and have been unable to obtain a rollback utility through normal Logitech support channels.

## Important

**Your mouse must be connected directly to the computer via USB for the DFU utility to detect it.**

Do not attempt the firmware operation over the wireless receiver or Bluetooth.

### Memory Profile Warning

**This rollback will reset the mouse's onboard memory profiles.**

After the rollback is complete, you will need to reconfigure your onboard profiles.

If you want to avoid using Logitech G HUB, use Logitech's **Onboard Memory Manager** application to configure DPI settings, button assignments, polling rate, and onboard profiles.

This is especially important because launching or using G HUB may prompt you to install the newer firmware again depending on your device and software configuration.

## Instructions

1. Download the ZIP file from this repository.
2. Extract the contents to a folder on your computer.
3. Locate the included `.exe` firmware utility.
4. Copy the full path to the executable.
5. Connect the mouse directly to the computer via USB.
6. Close Logitech G HUB if it is running.
7. Open **Command Prompt** or **PowerShell**.
8. Run the executable with the following parameters:

```text
update --entity all
```

Example:

```text
"C:\Users\%username%\Downloads\logivet-c095_16\logivet-c095_16.exe" update --entity all
```

If your extracted folder is located somewhere else, replace the path above with the actual path to the executable.

## After the Rollback

Once the firmware rollback is complete:

1. Your previous onboard memory profiles may be cleared or reset.
2. Download or open Logitech **Onboard Memory Manager**.
3. Reconfigure your DPI stages, polling rate, button assignments, and other onboard settings.
4. Save those settings directly to the mouse's onboard memory.

If your goal is to remain on the older firmware, I recommend using Onboard Memory Manager instead of G HUB for future configuration.

## USB / DFU Requirement

If the utility does not detect your mouse:

* Confirm that the mouse is physically connected by USB.
* Try connecting it directly to the computer instead of through a USB hub.
* Close Logitech G HUB before running the utility.
* Reopen the terminal and run the command again.

## Why This Repository Exists

The firmware update that prompted this repository caused severe tracking problems on my device. Because Logitech's normal software required the firmware update before allowing device configuration, rolling back through G HUB was not an available option.

After repeatedly requesting a rollback method from Logitech Support, I was eventually provided this firmware package.

Since other users may encounter the same issue, I am preserving the package and the recovery instructions here.

## Disclaimer

This repository is not affiliated with, endorsed by, or maintained by Logitech.

The firmware utility and firmware files were provided to me by Logitech Support. I did not create, modify, reverse engineer, or otherwise alter the firmware package.

Firmware flashing always carries some risk. Use this package at your own discretion and make sure the device remains connected during the update process.

Verify that the firmware package is appropriate for your specific mouse model before proceeding.

## Credits

All Logitech software, firmware, product names, trademarks, and related intellectual property belong to Logitech and their respective owners.

This repository exists solely to document and preserve a recovery procedure for affected users.
