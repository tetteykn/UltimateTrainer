# 🌟 Ultimate Games kernel Trainer
A versatile multi-game kernel-level trainer designed to support multiple games from a single application. Unlike traditional trainers that require a separate download for each game, this trainer contains all supported game profiles in one place. Simply select your game from the list and launch the desired features.

---

## ✅ Features

**Multi-Game Architecture**
All supported games are accessible through a single trainer application. There is no need to download a separate trainer for each game. As new game profiles are added, they become available directly within the trainer.

**Dynamic Address Resolution**
The trainer dynamically locates addresses via code injection rather than relying on static pointers, improving compatibility across game updates. It also supports pattern-based scanning with wildcard support (e.g. `8b 41 ? 89 42 ? f3 0f 2c 4b`) fully compatible with Cheat Engine's pattern format, allowing precise and flexible memory scanning across different game versions. This approach also ensures compatibility with emulators such as CEMU and PCSX2 — as long as the same emulator version is used, since the trainer locates addresses by scanning for known byte patterns at runtime, which naturally change every time the game or emulator is restarted.

**Automatic Address Updates**
Configuration files automatically update address locations when game updates change memory layouts, provided the target byte patterns remain unchanged.

**Teleport Manager**
Save and load player positions with unlimited slots. Locations can be exported, shared, edited, and backed up using text-based files.

**Advanced Hotkey System**
Supports complex hotkey combinations, hold and toggle modes, and customizable activation methods.

**Driver-Based Memory Access**
The trainer utilizes a custom kernel-mode driver for memory access, providing compatibility with a wide range of supported games. If the driver cannot be loaded, the trainer can also operate in User Mode as a fallback, although functionality may be limited depending on the game.


**Dynamic Interface**
The trainer can automatically display configured hotkeys, descriptions, and game-specific options directly within the interface.

---

## 🖥️ Standard Version
The Standard Version is designed for users who want a ready-to-use experience.

- No manual configuration required.
- Game profiles are pre-configured by the development team.
- The trainer automatically downloads and updates supported game profiles.
- Users simply select a supported game and begin using available features.
- All supported games are accessible from a single trainer application.

### 🔖 Trial System
The Standard Version includes a trial period.

During the trial period:
- All available game profiles can be tested.

After the trial period expires:
- Free game profiles remain accessible permanently.
- Premium game profiles require a one-time purchase before they can be used.
- Once purchased, a game profile is permanently added to the user's owned games list.
- Purchased game profiles remain permanently available on the licensed device.

---

## ⚙️ Personal Offline Version
The Personal Offline Version is intended for advanced users who want complete control over their own configurations.

Features include:
- Fully customizable hotkeys.
- Custom process names.
- Offline operation.
- User-created game profiles.
- Dynamic address descriptions.
- Custom memory modifications and code injections.

### 📝 Creating Personal Game Profiles
Users are responsible for finding addresses and cheats themselves using tools such as Cheat Engine.

After locating the desired addresses, users create a JSON configuration file containing the required information for the trainer. The trainer then loads and manages these configurations automatically.

Depending on the desired modification, users may configure memory value edits, byte patches, NOP instructions, code injections, hotkeys, descriptions, and other trainer settings directly through the JSON configuration.

Users may also share and use community-created profiles where available.

For a step-by-step guide on how to find cheats and configure them in the trainer, refer to this [video guide](https://youtu.be/fSJHGF4dwqM).

---

## 🔧 Driver Loading and Transparency
The trainer uses a custom kernel-mode driver for memory access.

By default, the driver is loaded through **TrainerAppLoader.exe**, which utilizes the [KdMapper](https://github.com/TheCruZ/kdmapper) project to load the driver during startup.

Because KdMapper-based loaders interact with Windows at a low level, some antivirus products may flag **TrainerAppLoader.exe** as suspicious or potentially unwanted software. This behavior is common for many driver-loading utilities and does not necessarily indicate malicious intent.

Users who do not wish to use the included loader are free to obtain the KdMapper source code from its official project page, review the source code themselves, compile their own version, and use it to load the trainer's driver (MemoryToolDriver.sys) manually.

After the driver has been loaded, users may launch the trainer directly using **TrainerAppLauncher.exe**.

We encourage users to verify any software they run on their systems and to use only trusted sources when obtaining third-party tools.

---

## 🛠️ Troubleshooting

### Driver Loading Issues

If the driver fails to load, follow these steps:

#### Step 1: Add Antivirus Exclusion
Create an exception for `TrainerAppLoader.exe` in your antivirus software.

#### Step 2: Disable Vulnerable Driver Blocklist

If the issue persists after adding the exclusion, you'll need to disable the Windows Vulnerable Driver Blocklist.

**Method 1: Using Registry Files (Recommended)**
1. Double-click `Disable Vulnerable Driver Blocklist.reg` to disable the blocklist.
2. Restart your PC.
3. To re-enable later, double-click `Enable Vulnerable Driver Blocklist.reg`.

**Method 2: Manual Registry Edit**
1. Open the Registry Editor (`regedit`).
2. Navigate to:
```text
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CI\Config
```
3. Double-click on `VulnerableDriverBlocklistEnable`.
4. Change the value from `1` to `0`.
5. Click **OK**.
6. Restart your PC.

> **⚠️ Important:** Remember to re-enable the blocklist after using the trainer to maintain system security.

#### Step 3: Restart Windows and Try Again

On some recent versions of Windows 11, the driver may fail to load even when the Vulnerable Driver Blocklist is disabled.

1. Restart Windows and try again.
2. If the driver still fails to load, restart Windows once more and try again.

> **Note:** Some systems may require multiple restarts before the driver loads successfully.

---

## 📜 Licensing
- Lifetime license for purchased game profiles.
- Non-transferable license.
- No refunds after purchase.
- Minimal anonymous hardware information is used solely for license validation.
- No personal information is collected.

---

## 👥 Community Profiles
Community-created game profiles may be shared and made available to other licensed users. Profiles are reviewed before being added to the trainer's profile library.

---

## 📌 Notes
This project has been under active development for several months and will continue to expand with additional game profiles and features over time.

The goal of this trainer is to provide a centralized platform where users can access multiple supported games from a single application instead of maintaining separate trainers for each title.

Whether you prefer a ready-to-use experience through the Standard Version or complete customization through the Personal Offline Version, the trainer is designed to offer flexibility while remaining easy to use.

---

## 📥 Download
[Ultimate Trainer](https://github.com/tetteykn/UltimateTrainer)

[Discord](https://discord.com/invite/jRnaeTJ)


