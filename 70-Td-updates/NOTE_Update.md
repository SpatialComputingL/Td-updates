# Virtual objects: SOP → POP conversion

**Status:** done, October 2, 2026

## What changed

- `virtual_object` and `virtual_object_viewer` now output **POPs instead of SOPs**. POPs run on the GPU, so scenes with many virtual objects run noticeably faster.
- Every virtual object gets its own colour. The viewer picks up all virtual objects automatically.
- The four separate calculation components (`DIST_between_points`, `DIST_to_object`, `IN_or_OUT_object`, `FADE_to_sphere`) are replaced by **one component: `CALC`**. Two POPs in, one CHOP out, one calculation at a time.
- Distance to a shape now works for every closed shape, and also between two shapes. Fade to sphere still needs a sphere with its outer shell on.

## What you need to do

- Replace the old calculation components in your patch with `CALC` and turn on the calculation you need.
- Update references to the output: the channels are now `center_dist`, `shell_dist`, `inside` and `fade`.
- Anything that still expects a SOP from `virtual_object` needs a POP version.
- Make sure your shapes are closed. An open side gives wrong distances.

## Documentation

- Every component in the toxes folder has a README next to it with the same name: `<tox name>-README.md`, e.g. `CALC-README.md`, `virtual_object-README.md`.
- The same READMEs are referenced inside the `.toe`, so you can also read them there.