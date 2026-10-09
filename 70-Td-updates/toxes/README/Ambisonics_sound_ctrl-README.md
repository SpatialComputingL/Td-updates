# Ambisonics sound control

Places sound sources in 3D space and mixes them for the ambisonics speaker system.
Each source has its own position, size and audio input.

In: one position per source (CHOP) · Out: mix for the speaker system

## How to use

1. Add a source with Add virtual object (+/-). A new inlet appears on the left.
2. Wire a position into that source's inlet, e.g. a virtual object. Inlets go top to bottom in the same order as the numbered sources.
3. Point Audio in at the CHOP that carries the sound.
4. Set Rangegain, or let a virtual object set it.

The network inside is built and wired by a script. Never rewire it by hand.

## Settings

- Add virtual object: adds or removes sources
- Posin: read-only readout of where the position comes from
- Rangegain: size and gain of the source. Follows the Radius of a wired virtual object (shown as a bind), otherwise type it in.
- Audio in: the CHOP or channel with the source's sound. Sample rates are matched to Dante (48 kHz) automatically.

## Outputs

- Ambisonics mix of all sources for the speaker system
- 3D view: one sphere per source, sized by Rangegain

## Normal, not bugs

- Posin shows the middle of the room: nothing wired into that source's inlet.
- Rangegain is a plain number instead of a bind: nothing wired in, or it isn't a virtual object.
- A new or removed source takes a moment to appear: the script rebuilds about once a second.
- A manual rewire inside the component reverts: the script puts the internal chain back.
