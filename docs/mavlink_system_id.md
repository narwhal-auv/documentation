# MAVLink System ID and Component ID

## Overview

Each system in the MAVLink network must have unique system ID, and each component within a system must have unique component ID. The ID are used to address a message to a particular system/ component and also used to message routing when components are on different network interfaces.

The pixhawk device or the FCU have a default system ID of 1, GCS like QGroundControl use a default system ID of 255, and MAVLink SDKs use an ID in the middle of the range. This `unique system id` ensures no message conflict.

FCU Parameters:

```bash
SYSID_THISMAV = 1
SYSID_MYGCS = 255
```

MAVROS is also a system of its own in the MAVLink network, so it needs a unique system ID. `In our case, NO, we don't use different system ID`. We want our MAVROS to act like GCS, so we set system ID of 255 to MAVROS node (or the same as SYSID_MYGCS value we set). [ManualControl](https://mavlink.io/en/messages/common.html#MANUAL_CONTROL]) message needs GCS system ID to works.