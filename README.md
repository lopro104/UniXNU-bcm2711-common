# UniXNU-bcm2711-common

Shared UniXNU support for the Broadcom BCM2711 (Raspberry Pi 4 Model B, Raspberry Pi 400, Compute Module 4):
`dts/bcm2711.dtsi` (GIC-400, PSCI, the `gpio` and `aux` nodes XNU's PI3_UART serial driver uses, disabled EMMC2 and
PCIe for the next drivers) and `configs/bcm2711.config` (GICv2, no PAN, native architectural timer).

`drivers/ArmCpu` is a submodule: [mouseos/ArmCpu](https://github.com/mouseos/ArmCpu), ArmCpu with the GICv2 (GIC-400)
path written for the MT8167 port. A driver folder here overrides UniXNU's own `drivers/ArmCpu`. Drop it once the GICv2
path is in UniXNU/ArmCpu.

Device repository: lopro104/UniXNU-rpi4.
