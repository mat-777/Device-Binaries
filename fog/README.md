## Patches/Fixes

### ButtonsDxe:

- Reason: Helps navigating Menus (e.g. UEFI Menu).
- Patch: Key code was patched for the power button to be mapped as ENTER instead of SUSPEND.
- Patch Creator: [Robotix22](https://github.com/Robotix22)

### ClockDxe (Temporary Patch):

- Reason: A Npa Node gets Registert wich kills Display.
- Patch: That Node Register has been removed to avoid killing Display.
- Patch Creator: [Kernel357](https://github.com/Kernel357) & [Robotix22](https://github.com/Robotix22)

### MinidumpTADxe:

- Reason: The TZ applet it already brought up.
- Patch: DXE were patched to not start again the TZ applet.
- Patch Creator: [Gustave Monce](https://github.com/gus33000)

### UFSDxe:

- Reason: An MMU Domain is already setup by the previous firmware and gets re-set again, causing a crash.
- Patch: MMU related setup routine was patched to not recreate already existing MMU domains.
- Patch Creator: [Gustave Monce](https://github.com/gus33000)

### SdccDxe:

- Reason: An MMU Domain is already setup by the previous firmware and gets re-set again, causing the driver to crash.
- Patch: MMU related setup routine was patched to not recreate already existing MMU domains.
- Patch Creator: [Robotix22](https://github.com/Robotix22)

### HALIOMMUDxe:

- Reason: IOMMUs for USB and eMMC are already present, If reset again UEFI crashes.
- Patch: IOMMU for USB and eMMC has been patched to always return Success.
- Patch Creator: [Robotix22](https://github.com/Robotix22)
