Here's an easier-to-read network diagram.

```mermaid
graph LR
    ISP --- ONT
    ONT -- Ethernet --> UDMPro((Unifi Dream Machine Pro))
    UDMPro -- LAN --> U6Lite((Unifi Access Point U6 Lite))
    U6Lite -- mesh --> U6Ext1((Unifi Access Point U6 Extender))
    U6Lite -- mesh --> U6Ext2((Unifi Access Point U6 Extender))
    U6Ext1 -- |Front| Guest House
    U6Ext2 -- |Back| Guest House
    Guest House -- fiber --> UnifiSwitch((Unifi Switch))
    UnifiSwitch -- Ethernet --> U6Lite
```
