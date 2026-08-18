
# Hardware-Level Firmware Extraction

So far, in the [initial_connect.md](../uart2_connect/initial_connect.md) there is documented just the interaction with the UART2 port which turns out is just a **Logging Port**. This port is for output-only, diagnostic text. However Beken chips have the dedicated **Flashing Port** (UART1) that might contain the Download Mode into the hardware.


The steps are the following:
1. Connecting some wires/probes to the UART1 RX/TX pins and GND. Also we have to connect the CEN pin (Chip Enable/Reset).
2. Connecting the camera to a USB to TTL adapter. Some readings suggest that for a flash read, the USB adapter cannot provide enough current and a steady 3.3V external alimentation is required (in case that one uses the USB, the dump might get corrupted)
3. Getting the Flashing Software. Finding a Python tool designed for the Beken chip and executing a full flash (the address depending on the model i believe)
4. Jumping the CEN pin to ground which will force a hard reset. Upon waking up, the chip's ROM intercepts the software's signal on UART1 and stops the boot sequence, locking it into Download Mode to dump the firmware. 