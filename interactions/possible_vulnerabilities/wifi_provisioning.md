# Wi-Fi Provisioning Exploit (CloudCutter)

The device relies on a smart-config protocol to receive the Wi-Fi password from the phone.

Some Beken SDKs are vulnerable to a buffer overflow in the pairing process. 

A public exploit known as [Tuya CloudCutter](https://github.com/tuya-cloudcutter/tuya-cloudcutter) can wirelessly inject a payload into the chip during the Soft-AP phase, allowing the attacker to completely overwrite the firmware over Wi-Fi. 