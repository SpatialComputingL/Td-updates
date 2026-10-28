# Floor projection

The output to the floor projector.
Works like Wall projection, but the floor is square-ish, not wide.

In: 1 TOP · Out: projection window and resolution (CHOP)

## How to use

1. Wire the resolution CHOP (resX, resY) into your source TOP.
2. Put a Fit TOP before the component:

```
moviefilein → fit → floor_projection
```

3. Press Configure.
4. Open Window to project, Close Window while editing.

## Settings

- License: off = home resolution, on = full lab resolution
- Fit Input: what happens to an image of the wrong size
- Configure: rebuilds after changing settings
- Open Window, Close Window: opens or closes the projection

## Outputs

- Resolution CHOP: resX, resY for your source

## Normal, not bugs

- Wall content looks wrong: different aspect ratio. Add a Fit.
- Small resolution: License is off.
- Image "upside down": the floor has no up. Orient to where the audience enters, and note it.
- Nothing visible after a change: Configure, then Open Window.
