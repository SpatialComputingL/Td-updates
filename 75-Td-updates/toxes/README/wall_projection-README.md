# Wall projection

The output to the lab's wall projectors.
Opens the projection window and tells you the resolution your image must have, at home and in the lab.

In: 1 to 3 TOPs · Out: projection window and resolution (CHOP)

## How to use

1. Wire the resolution CHOP (resX, resY) into your own source TOP. Don't type numbers.
2. Wire your images in: input 1 left, 2 center, 3 right.
3. Choose a mode and press Configure.
4. Open Window to project, Close Window while editing.

## Settings

- License: off = home resolution, on = full lab resolution
- Panoramic projection: one wide image across the wall, uses input 1 only
- Single projection: output to one projector only
- Both off: three screens, left, center, right
- Fit Input: what happens to an image of the wrong size
- Output Resolution: readout of the current resolution
- Configure: rebuilds after changing mode
- Open Window, Close Window: opens or closes the projection

## Outputs

- Resolution CHOP: resX, resY for your source

## Normal, not bugs

- Small resolution: License is off (home setting).
- Inputs 2 and 3 do nothing: Panoramic is on.
- Stretched, cropped or black bars: your source isn't following the resolution CHOP.
- Content on the wrong wall: order is left, center, right.
- Nothing visible after a change: Configure, then Open Window.
