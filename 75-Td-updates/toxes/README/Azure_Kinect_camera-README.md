# Camera - Azure Kinect

The live camera image of the lab's Azure Kinect sensors.
Image only: the video stream comes from a different PC.
For body positions, use Sensor - Azure skeleton.

In: none · Out: one TOP per sensor

## How to use

1. Pick a stream in Image.
2. Press Configure.
3. Hang a named null off each outlet (null_cam_left, null_cam_right, ...) and work from those.

## Settings

- Image: which stream you get (colour, ...)
- Configure: rebuilds the outlets after changing Image

## Outputs

- Outlet 1, 2, 3: one sensor each, fixed order. Wave at a camera to find out which is which.

## Normal, not bugs

- Black or empty outputs: not in the lab, or the sensors are off.
- All views look the same: the same empty room from different corners.
- Image doesn't change after switching Image: press Configure.
- Unexpected resolution or framerate: set by the sensor and stream. Fit or resample downstream.
