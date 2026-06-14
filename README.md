## Fixes for TP-Link X80-5G
Personal repo for the X80-5G. 

The 5G modem in TP-Link Deco X80-5G defaults to PCIe mode. This means it will only work in PPP mode, unless you either:
- Enable the radio fully (GPIO 55)
- Either: Change modem to USB mode (AT+QCFG="data_interface",0,0) and enable QMI or MBIM (AT+QCFG="usbnet",0 for QMI AT+QCFG="usbnet",2 for MBIM)
- Or: Leave modem in PCIe mode and make sure you have compiled OpenWRT with MHI 


The modifications in this repo change modem w_disable state pin to reflect the one used in original TP-Link DTS file and add pcie support. 
Reasons for this can be found in [forum thread](https://forum.openwrt.org/t/issues-enabling-modem-on-tp-link-deco-x80-5g-not-working/250907)

That is all. 

<img src="include/ihniwid.jpg" alt="disclaimer" title="I have no idea what I'm doing &trade;" width="200"/>



## License

OpenWrt is licensed under GPL-2.0
