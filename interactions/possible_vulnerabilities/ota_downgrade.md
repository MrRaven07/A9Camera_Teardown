# Over-The-Air (OTA) Downgrade Attack

The OTA manager is responsible for writing updates to the flash. This might lack "anti-rollback" protection.

An attacker can intercept the network traffic and impersonate the manufacturer's OTA server following a forced "upgrade" to an older version.

