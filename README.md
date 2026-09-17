# ballon-tapper

An Android overlay that watches the screen, finds balloons by colour and taps them.
The whole app is generated and built by `.github/workflows/build.yml` — run that
workflow and download the `BalloonTapper-apk` artifact.

## Play style

The tapper can play as a machine or as a person. Pick one in the app before
launching the overlay (the floating button shows which style is running).

- **Machine** — the original behaviour: taps the instant a balloon is detected,
  dead centre, at a fixed rhythm, with no pauses.
- **Human — casual** *(default)* — takes about a quarter of a second to notice a
  balloon, aims somewhere on it instead of at its centre, moves one finger from
  balloon to balloon, taps two or three at a time, fumbles one now and then,
  walks past a balloon it should have popped, pauses every few seconds and slows
  down over a long session.
- **Human — focused** — the same, quicker and steadier: faster reactions, tighter
  aim, fewer misses and shorter breaks.

The tap speed and fixed-gap settings only apply to the machine style; the human
styles work out their own timings.
