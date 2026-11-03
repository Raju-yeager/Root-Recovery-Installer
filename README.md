<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:ff0055&height=230&section=header&text=AEGIS-ROOT&fontSize=65&fontColor=ffffff&animation=twinkling&fontAlignY=35&desc=%E2%9A%A1%20Universal%20GKI%202.0+%20Root%20%26%20SuSFS%20LKM%20Auto-Patcher%20%E2%9A%A1&descAlignY=60&descSize=18" width="100%" alt="AegisRoot Banner"/>

<a href="https://github.com/Raju-yeager/SukiSU-Ultra-Flasher">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=20&duration=3000&pause=800&color=FF0055&center=true&vCenter=true&width=780&lines=Universal+Recovery-Flashable+Root+Installer;SukiSU-Ultra+%2B+KernelSU-Next+%2B+SuSFS+LKM;AVC+Log+Spoofing+%26+SELinux+Stealth+Out-of-the-Box;Auto-Patches+init_boot+%2F+boot+%26+Auto-Installs+Spoofed+APK;Maintained+by+%40Raju_D_yeager" alt="Typing SVG" />
</a>

<br/>

[![Maintainer](https://img.shields.io/badge/Maintainer-%40Raju__D__yeager-ff0055?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Raju-yeager)
[![Telegram Channel](https://img.shields.io/badge/Telegram-Izanami__kernel%20(peridot)-0088cc?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/Evil_twin_peridot)
[![SukiSU Builder](https://img.shields.io/github/actions/workflow/status/Raju-yeager/SukiSU-Ultra-Flasher/build-flasher.yml?style=for-the-badge&logo=linux&label=SukiSU-Ultra%20CI&color=7928CA)](https://github.com/Raju-yeager/SukiSU-Ultra-Flasher/actions)
[![KSUN Builder](https://img.shields.io/github/actions/workflow/status/Raju-yeager/SukiSU-Ultra-Flasher/build-ksun.yml?style=for-the-badge&logo=android&label=KSUN%20CI&color=00F5D4)](https://github.com/Raju-yeager/SukiSU-Ultra-Flasher/actions)
[![Latest Release](https://img.shields.io/github/v/release/Raju-yeager/SukiSU-Ultra-Flasher?style=for-the-badge&logo=github&color=FFbe0b&label=Latest%20Drop)](https://github.com/Raju-yeager/SukiSU-Ultra-Flasher/releases/latest)

<br/>

<img src="https://img.shields.io/badge/Android%2014-6.1%20GKI-3DDC84?style=flat-square&logo=android&logoColor=black"/>
<img src="https://img.shields.io/badge/Android%2015-6.6%20GKI-00E5FF?style=flat-square&logo=android&logoColor=black"/>
<img src="https://img.shields.io/badge/Android%2016-6.12%20GKI-B388FF?style=flat-square&logo=android&logoColor=black"/>
<img src="https://img.shields.io/badge/Android%2017-6.18%20GKI-FF4081?style=flat-square&logo=android&logoColor=white"/>
<img src="https://img.shields.io/badge/SuSFS-LKM%20Integrated-FF6D00?style=flat-square&logo=securityscorecard&logoColor=white"/>

</div>

---

## 🔥 What is AegisRoot?

**AegisRoot** is a zero-hassle, universal recovery-flashable root & stealth installer designed for custom ROM and custom kernel enthusiasts. Instead of manually extracting `init_boot.img`, patching it in an app, flashing via `fastboot`, and hunting down matching SuSFS modules, **you just flash one ZIP in TWRP / OrangeFox / Aera Recovery and reboot.**

It works on **any custom or stock GKI 2.0+ kernel** (Vibranium, Izanami, Melt, stock HyperOS, AOSP, LineageOS, etc.) across all modern Snapdragon, MediaTek, and Tensor devices.

---

## ⚡ Core Arsenal & Stealth Features

* 🧠 **Smart KMI & Slot Auto-Detection:** Reads `uname -r` live inside recovery to match your exact kernel (`android14-6.1`, `android15-6.6`, `android16-6.12`, or `android17-6.18`) and automatically targets your active `_a` / `_b` slot (`init_boot` preferred, falls back to `boot`).
* 👻 **SuSFS LKM Pre-Wired (`susfs_guard_lkm.ko`):** Automatically drops the matching SuSFS LKM into `/data/adb/susfs4ksu/` and loads it at `post-fs-data.d` with `expose_proc=1` so the Manager GUI has full control from your very first boot.
* 🛡️ **Out-of-the-Box Stealth Flags:**
  * **AVC Log Spoofing (`ENABLE_AVC_SPOOF=1`):** Blocks root detectors from sniffing SELinux audit log denials.
  * **Hide SELinux Modifications (`ENABLE_HIDE_SELINUX=1`):** Masks policy `seqno` changes from banking and integrity detectors.
* 📦 **Bulletproof Spoofed APK Auto-Installer:** Bundles the official **Spoofed Manager APK** for *both* SukiSU-Ultra and KernelSU-Next, streaming it silently via `/data/local/tmp` once Android boots—bypassing Xiaomi/HyperOS USB install blocks and SELinux denials.
* 🤖 **Autonomous CI/CD + Telegram Sync:** GitHub Actions monitors upstream SemVer releases daily, builds fresh unstripped packages, publishes to GitHub Releases, and drops them straight into [**@Evil_twin_peridot**](https://t.me/Evil_twin_peridot).

---

## 📊 Dual-Engine Build Matrix

| Feature / Component | 💜 **AegisRoot SukiSU-Ultra Edition** | 💚 **AegisRoot KernelSU-Next Edition** |
| :--- | :--- | :--- |
| **Core Root Engine** | `SukiSU-Ultra` (`ksud` + `kernelsu.ko`) | `KernelSU-Next` (`ksud` + `kernelsu.ko`) |
| **SuSFS LKM (`inforcqb`)** | ✅ Pre-staged + Early Load | ✅ Pre-staged + Early Load |
| **Bundled Manager APK** | ✅ **Spoofed Package APK** (Auto-Installed) | ✅ **Spoofed Package APK** (Auto-Installed) |
| **AVC Log Spoofing** | ✅ Enabled by Default | ✅ Enabled by Default |
| **Hide SELinux Mod** | ✅ Enabled by Default | ✅ Enabled by Default |

---

## 🚀 Flash Instructions (TWRP / OrangeFox / Aera Recovery)

1. **Download your preferred engine** (`SukiSU_Ultra_*_Universal_Installer.zip` or `KernelSU_Next_*_Universal_Installer.zip`) from [**GitHub Releases**](https://github.com/Raju-yeager/SukiSU-Ultra-Flasher/releases) or [**Telegram (@Evil_twin_peridot)**](https://t.me/Evil_twin_peridot).
2. **Boot into Custom Recovery** (Aera / OrangeFox / TWRP) and unlock/decrypt `/data` with your lockscreen PIN/pattern.
3. *(Optional but recommended)* Backup your current `init_boot` / `boot` partition.
4. **Flash the ZIP** -> Reboot to System.
5. Wait ~5 seconds after unlocking your screen—the bundled **Spoofed Manager** app will appear in your app drawer automatically with **Working (LKM)** + **SuSFS** active!

---

## ⚙️ Customizing Stealth Toggles (`config.env`)

Want manual control over stealth flags before flashing? Open the `.zip` in **ZArchiver** and edit `config.env` at the root of the archive:

```ini
ROOT_VARIANT="SukiSU-Ultra"
ENABLE_SUSFS_LKM=1
ENABLE_SUSFS_EARLY_LOAD=1
ENABLE_AVC_SPOOF=1
ENABLE_HIDE_SELINUX=1
```

*(Set any option to `0` to disable automatic boot-time activation).*

---

## 🌐 Community & Credits

* 👤 **Maintainer & Developer:** [**@Raju_D_yeager**](https://github.com/Raju-yeager)
* 📢 **Official Telegram Channel:** [**Izanami_kernel (peridot) — @Evil_twin_peridot**](https://t.me/Evil_twin_peridot)
* 🙏 **Upstream Credits:**
  * [SukiSU-Ultra Team](https://github.com/SukiSU-Ultra/SukiSU-Ultra)
  * [KernelSU-Next (`rifsxd`)](https://github.com/KernelSU-Next/KernelSU-Next)
  * [SuSFS for LKM (`simonpunk` / `inforcqb`)](https://github.com/inforcqb/susfs4ksu-for-lkm)
  * [Magisk (`topjohnwu`)](https://github.com/topjohnwu/Magisk)

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:ff0055&height=110&section=footer" width="100%"/>
</div>
