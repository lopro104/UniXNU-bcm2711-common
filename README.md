# UniXNU-bcm2711-common

Shared UniXNU support for the Broadcom BCM2711 (Raspberry Pi 4 Model B, Raspberry Pi 400, Compute Module 4):
`dts/bcm2711.dtsi` (GIC-400, PSCI, the `gpio` and `aux` nodes XNU's PI3_UART serial driver uses, disabled EMMC2 and
PCIe for the next drivers) and `configs/bcm2711.config` (GICv2, no PAN, native architectural timer).

`feeds.toml` names the GICv2 ArmCpu fork, but a git source ranks below UniXNU's own `drivers/ArmCpu`: it takes
effect only as a `drivers/ArmCpu` checkout (submodule) in this repository.

Device repository: lopro104/UniXNU-rpi4.
