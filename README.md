# Hackintosh-OpenCore

# HP EliteBook 1040 G4 with OpenCore

### Status: Running

Currently running:

| Component     | Version      |
| ------------- | ------------ |
| macOS version | 11.3.1 (20E241 |
| OpenCore      | 0.6.9        |
| BIOS version  | 1.38        |

## Hardware info

| Component | Model                                   |
| --------- | --------------------------------------- |
| CPU       | Intel(R) Core(TM) i7-7820HQ CPU @ 2.90GHz / KabyLake    |
| Memory    | 16GB                       |
| Storage   | Samsung MZVLW512HMJP-000H1                 |
| Display   | 14" 1920x1080                 |
| GPU       | Intel HD Graphics 630                          |
| WLAN      | Intel Wireless 8265 |

## Status

### Working

- [x] Keyboard (including all media keys)
- [x] Battery indicator (number of cycles reported)
- [x] Display brightness (keys F3 and F4)
- [x] Audio (only 2 speakers on ALC Layout ID 22, other channel 21 is providing more speakers and better sound quality but not working anymore after sleep/wake cycle)
- [x] Ethernet
- [x] iCloud services - iMessage, FaceTime, AppStore
- [x] Camera
- [x] Microphone
- [x] Bluetooth
- [x] Sleep/wake (˜4% of power consumption after 12 hours of sleep)
- [x] Trackpad and some gestures
- [x] HDMI video

### Working, sort of

- [ ] Wifi works but not at full speeds with Heliport/itlwm
- [ ] USB-C video output works, but no audio

## Compatible BIOS settings

| Parameter     | Value      |
| ------------- | ------------ |
|TPM Device | Hidden |
|TPM State | Disable |
| TPM Activation Policy | No prompts |
|Fast Boot | Disable |
|Network (PXE) Boot | Disable |
| Configure Legacy Support and Secure Boot | Legacy Support Disable and Secure Boot Disable |
| HP Application Driver | Disable |
| Wake On LAN | Disabled |
| Extended Idle Power States | Enable |
| Wake when Lid is Opened | Enable |
| Fingerprint Device | Disable |
| Video Memory Size | 128 MB |
| Intel Software Guard Extensions (SGX) | Disable |
| Virtualization Technology (VTx) | Disable |
| Virtualization Technology for Directed I/O (VTd) | Disable |
| Deep Sleep | On |

## Post-install

sudo pmset autopoweroff 0
sudo pmset powernap 0
sudo pmset standby 0
sudo pmset proximitywake 0
sudo pmset tcpkeepalive 0

Install Heliport for WIFI

## CREDITS

- [Acidanthera](https://github.com/acidanthera)
- [Dortania OC guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [Rehabman's battery patch guide](https://www.tonymacx86.com/threads/guide-how-to-patch-dsdt-for-working-battery-status.116102/) and [Rehabman's ACPI hotpatching guide](https://www.tonymacx86.com/threads/guide-using-clover-to-hotpatch-acpi.200137/)
- [OpenWireless and itlwm](https://github.com/OpenIntelWireless/itlwm)
