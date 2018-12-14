# Configuring Ubiquiti Bullet M2 as Bridge

The Bullet M2 is a Wi-Fi device capable of operating as Station, Access-Point, Router, Bridge, among many other configurations.
Due to its high power antenna and output, it is capable of long range communications, and thus suited to missions with boats,
drones and other robots with large areas of operation.

![](https://http2.mlstatic.com/ubiquiti-bullet-m2-hp-outdoor-24ghz-600mw-novo-original-D_NQ_NP_695248-MLB26399915191_112017-F.jpg "Bullet M2")

This tutorial describes the step-by-step configuration of this device in Bridge mode, where the connection between wireless and ethernet devices
is established.

## Powering up the Bullet

The Bullet M2 operates via Power-over-Ethernet (PoE).
If your device does not support PoE, an adapter setup must be used, as shown below (even though the modem is not a Bullet M2, the same setup applies).

![](https://prd-www-cdn.ubnt.com/media/images/product-features/poeadapters-feature-device-protection-small2x.jpg "PoE Adapter Setup")


## Configure Bullet WLAN as Access Point

To enable WiFi communication with wireless devices, the Bullet's WLAN must be configured as Access Point.
Follow [this tutorial](https://platypus-boats.readthedocs.io/en/latest/source/rpi/peripheral/bullet-m2.html), up to (and including) part "Configuring the Bullet M2HP as an Access Point".


## Configure Bullet Bridge Mode

A main limitation of the Bullet M2 is that to run a DHCP server (automatically assign IPs to connecting devices), the module "Network" must be set as a Router.
This causes WLAN and LAN to be separated, thus isolating whatever device is connected to the Bullet's PoE port.
To avoid this, the network must be set to "bridge" mode, which kills the DHCP server, requiring manual or external IP assignment.

The solution is to manually change the Bullet's configuration file to enable the DHCP server to run in bridge mode.
To do this, using a computer (based on [this](https://community.ubnt.com/t5/airOS-Software-Configuration/Bullet-m2-DHCP-server-on-Wireless-and-LAN/m-p/155659/highlight/true#M13345) forum post):

  * Connect to the Bullet's WiFi network created in the last step and access the device's configuration page (typically through IPs "192.168.1.20" or "192.168.1.1").
  * On the "System" tab, download the device's configuration with the "Backup configuration" download button.
  ![](http://3.bp.blogspot.com/-pnXkDu_y1JM/UKA2Ksxn0_I/AAAAAAAAI3s/zTTrMTTIbPg/s1600/Ubnt+System+Screen.JPG "Bullet M2 System Configuration")
  
  * Open the downloaded .cfg file and add the following lines (some may not exist, in which case, just add them):
  
  ```
  dhcpd.status=enabled
  dhcpd.1.status=enabled
  dhcpd.1.start=192.168.1.100
  dhcpd.1.netmask=255.255.255.0
  dhcpd.1.lease_time=36000
  dhcpd.1.end=192.168.1.200
  dhcpd.1.dnsproxy=enabled
  dhcpd.1.devname=br0
  dhcpc.status=disabled
  dhcpc.1.status=disabled
  dhcpc.1.devname=br0
  ```
  
  * Save the file, go back to the System tab on the Bullet M2 configuration webpage and use the "Upload configuration" option to upload the modified .cfg.
  * Press "Apply" on the top of the page for the changes to take effect.
  
## Configuring your Ethernet device

**Not confirmed if needed, adding here just to be safe**

Although the Bullet now operates with DHCP in bridge mode, the IP of the Ethernet device may need to be manually set.
To avoid this, on the ETH device, follow [this step](https://platypus-boats.readthedocs.io/en/latest/source/rpi/peripheral/bullet-m2.html#testing-the-connection-between-wifi-and-the-raspberry-s-ethernet) from the previously mentioned tutorial.
