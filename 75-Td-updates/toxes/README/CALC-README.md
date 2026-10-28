# Calculations

Measures how a point or shape relates to another point or shape:
distance, inside or outside, or a fade.
Typical use: a tracked hand and a virtual object.

In: 2 POPs (point or shape) · Out: 1 CHOP

## How to use

1. Connect a point or shape to input 1, e.g. a tracked joint.
2. Connect a point or shape to input 2, e.g. a virtual object.
3. Turn on one calculation.
4. Read the result from the output CHOP.

## Settings

- Distance between points: distance between the centers of both inputs
- Distance between shapes: distance to the surface of the shape(s)
- In or outside of a shape: is input 1 inside input 2
- Fade to sphere: soft value between the inner sphere and the outer shell

Only one can be on. The others grey out until you turn it off.

## Outputs

- center_dist: meters between the centers
- shell_dist: meters to the surface, negative = inside
- inside: 1 inside, 0 outside
- fade: 1 inside the inner sphere, 0 outside the outer shell, smooth in between

## Normal, not bugs

- Fade to sphere greyed out: input 2 is not a sphere with Outer shell on.
- Wrong distances: the shape is not closed (open side).
- Box or cylinder distances a bit large near edges and corners: measured from the center outward.
- Yellow warning inside the component with a point on input 1: harmless.
