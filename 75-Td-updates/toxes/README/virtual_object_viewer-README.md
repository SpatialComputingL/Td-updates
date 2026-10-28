# Virtual object viewer

Shows tracked points and virtual objects together in one 3D scene,
to check that everything is where you think it is.
It only displays, it changes no data.

In: positions (CHOP) and shapes (POP) · Out: preview

## How to use

1. Wire joint outlets of Sensor - Azure skeleton into the green inputs. Each becomes a sphere.
2. Virtual objects in the project appear with their own colour.
3. Pick a Viewport.

## Settings

- Viewport: perspective for a quick check, top for the floor plan
- Colors: off = grey, on = coloured

## Outputs

- Preview: 3D scene, the wireframe box is the room

## Normal, not bugs

- Everything in one spot: nothing wired, or the sensor isn't running.
- Spheres frozen: the source is frozen. Check the sensor.
- A sphere outside the box: position out of range, or outside the sensor's field.
- Low-resolution preview: it's a node preview. Open a bigger viewer.
