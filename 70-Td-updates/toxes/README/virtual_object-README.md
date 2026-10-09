# Virtual object

Puts an invisible shape (sphere, box, cylinder) in the room for other components to interact with.

In: position (CHOP, optional) · Out: shape (POP) and position + size (CHOP)

## How to use

1. Pick a shape in Virtual Object.
2. Set the size, Position XYZ and Rotate XYZ.
3. Wire the blue output into Calculations or Virtual object viewer.
4. Wire the green output into anything that needs the position, e.g. a sound source.

## Settings

- Virtual Object: shape, sphere, box or cylinder
- Width X, Height Y, Depth Z, Radius: size. Only the fields for the current shape are active.
- Position XYZ, Rotate XYZ: place in the room (X = width, Y = height, Z = depth)
- Get pos (shift+m): grab a position instead of typing it
- Outer shell + Radius: sphere only, a larger outer sphere for a soft edge, used by Fade to sphere
- Viewport: preview camera only, doesn't move the object

## Outputs

- Blue: the shape as a POP
- Green: center position tx ty tz and a size value from the radius

## Normal, not bugs

- Size fields greyed out: they belong to another shape.
- Outer shell greyed out: not a sphere.
- Preview looks squashed or off-centre: that's the viewport. Switch it.
- Nothing visible in the room: this only makes the shape. Draw it with the viewer or a projection.
