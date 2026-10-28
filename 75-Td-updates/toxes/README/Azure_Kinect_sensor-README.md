# Sensor - Azure skeleton

Live 3D positions of body joints from the Azure Kinect sensors.
Choose the joints you need, each gets its own outlet.

In: none · Out: one CHOP per joint (tx ty tz)

## How to use

1. Add joints (+/-) and pick a joint in each slot (head, hand_l, hand_r, pelvis, ...).
2. Press Configure.
3. Hang a null named after the joint off each outlet (null_head, null_handl, ...).
4. Not in the lab? Turn on Mouse and keep building.

## Settings

- Mouse: off = sensor data, on = joints follow the mouse
- Mouse orientation: which plane the mouse drives (XZ = across the floor)
- Add joints: adds or removes joint slots
- Configure: rebuilds the outlets after changing joints
- Person: not working yet, leave at 1
- Fallback origin: joints rest at Position when there is no data

## Outputs

- One outlet per slot: tx ty tz in meters, same order as the slots
- Axes: X = width, Y = height, Z = depth

## Normal, not bugs

- All values 0: not in the lab, or nobody in view. Turn on Mouse.
- Mouse orientation greyed out: Mouse is off.
- Person does nothing: known, see above.
- Values jump when someone re-enters: tracking re-acquiring. Use Fallback origin or smooth downstream.
- Removed joints still showing: press Configure.
