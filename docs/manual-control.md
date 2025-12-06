# Manual Control

We can manual control the Ardusub with mavlink protocol called [MANUAL_CONTROL](https://mavlink.io/en/messages/common.html#MANUAL_CONTROL). That mavlink protocol can be used from ros2 environment with mavros. The MANUAL_CONTROL is exposed in ros2 topic: `/mavros/manual_control/send`

## How to Give Command

1. Launch the narwhal_comms

```bash
ros2 launch narwhal_comms comms.launch.py
```

2. If you want to control with joystick

```bash
ros2 launch narwhal_joy joy.launch.py
```

List of Button:

- Axis 1: Left Stick Vertical (Forward/Backward) -> x
- Axis 0: Left Stick Horizontal (Left/Right) -> y
- Axis 7: D-pad Vertical (Up/Down) -> z (Depth)
- Axis 2: Right Stick Horizontal (Yaw) -> r
- button A: ARMING
- button B: DISARMING
- button X: MANUAL
- BUTTON Y: STABILIZE

Netral Value

- x = 0.0
- y = 0.0
- z = 500.0
- r = 0.0

For testing purpose:  

```bash
ros2 topic pub /mavros/manual_control/send mavros_msgs/msg/ManualControl \
"{x: 500.0, y: 0.0, z: 500.0, r: 0.0, buttons: 0}"

```