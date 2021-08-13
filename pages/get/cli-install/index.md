---
title: Commandline Installer
description: 🥳 You're amazing! Follow the instructions below to install CalyxOS!
---

<div class="alert alert-info" markdown="0">
<b>NOTE:</b> In the USA there are two variants of the Google Pixel phones: The Google unlocked version, and the Verizon one. The Verizon one is unfortunately locked in such a way (boot loader locked) that you cannot install another operating system on it. The only way to tell is to attempt to unlock the bootloader of the phone. If you can enable "OEM unlocking" then it's an unlocked version. If "OEM unlocking" is greyed out and not toggle-able then you have the Verizon version.
</div>

## Download Device Flasher

| OS | Download | SHA256 Digest |
| ---- | ---- | ---- |
| Linux | [device-flasher.linux](https://release.calyxinstitute.org/device-flasher/1.0.3/device-flasher.linux) | f4e68992198868148ca2d4bd0fd40d0176da4058a188a3fdf80732d04a6c3543 |
| macOS | [device-flasher.darwin](https://release.calyxinstitute.org/device-flasher/1.0.3/device-flasher.darwin) | 5e5542f51c1592e392114636f2e64fe9dae1cacaaf55c722822780ec5cbf9331 |
| Windows | [device-flasher.exe](https://release.calyxinstitute.org/device-flasher/1.0.3/device-flasher.exe) | 0cdaf47f1c97e43c70e0fe7cfff63fcaa140799ccc494bebf6451e96cbcdda6c |

## Installation Steps

1. **Download Image**: Make sure you have the correct CalyxOS image for your device from [[Get CalyxOS => get]].
2. **Download device-flasher**: Using the links above, download `device-flasher` for your operating system.
  * For Windows, you also need to download and install [Googles USB driver ZIP file](https://developer.android.com/studio/run/win-usb) ([instructions](https://developer.android.com/studio/run/oem-usb#InstallingDriver)).
3. **Verify checksum**:
   * Windows: `CertUtil -hashfile device-flasher.exe SHA256`
   * Linux: `sha256sum device-flasher.linux`
   * macOS: `sha256sum device-flasher.darwin`

    Ensure that the checksum returned matches the corresponding checksum in the above table.

4. **Put together**: Place `device-flasher` as well as the CalyxOS .zip image into the same folder. Do not extract or rename the zip, simply copy it as-is.

5. **Run it**:
   * **Windows**:
     * Double-click `device-flasher` to run it and follow the steps shown on your screen.
   * **Linux**:
     * Open a terminal and navigate to the directory where you placed device-flasher and the CalyxOS zip image.
     * Make the installer executable: `chmod +x ./device-flasher.linux`
     * Then start the installer: `sudo ./device-flasher.linux`
   * **macOS**:
     * Open a terminal and navigate to the directory where you placed device-flasher and the CalyxOS zip image.
     * Make the installer executable: `chmod +x ./device-flasher.darwin`
     * Then start the installer: `sudo ./device-flasher.darwin`

## Notes
* On macOS, you may have to disable gatekeeper. See ["How to open an app that hasn’t been notarized or is from an unidentified developer"](https://support.apple.com/en-us/HT202491).
* On Windows, your anti-virus may falsely flag this as infected. This is because the program is written in the Go programming language, see [Golang docs](https://golang.org/doc/faq#virus) for more information.
