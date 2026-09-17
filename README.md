# ballon-tapper

An Android overlay that watches the screen, finds balloons by colour and taps them.
The whole app is generated and built by `.github/workflows/build.yml` — run that
workflow and download the `BalloonTapper-apk` artifact.

## Play style

The tapper can play as a machine or as a person. Pick one in the app before
launching the overlay (the floating button shows which style is running).

- **Machine** — the original behaviour: taps the instant a balloon is detected,
  dead centre, at a fixed rhythm, with no pauses.
- **Human — casual** — about 4 taps a second in a burst, in no rush between them:
  a quarter-second to notice a balloon, aim scattered over it, one finger moving
  from balloon to balloon, the odd fumble, a balloon walked past now and then,
  a short break every few seconds and a slow drift toward slower.
- **Human — focused** *(default)* — the same person playing properly: 6-7 taps a
  second, faster reactions, tighter aim, fewer misses, shorter breaks.
- **Human — rapid** — flat out, around 10 taps a second, barely stops. That is the
  top of what a hand really manages, and the aim loosens to pay for it, so more
  taps land off the balloon than on focused.

Each human style also warms up over its first few seconds, occasionally taps a
balloon twice when unsure it registered, and now and then overshoots a far
balloon and darts back — all things a real hand does. The speed you get comes
from short gaps between bursts, not from a faster peak tap rate, so it clears
more without tapping any less like a person.

While the overlay is running there are two floating buttons: the main
START/STOP button, and a **⚡ TURBO** button. Human play uses two thumbs; tap
TURBO in the last few seconds of a round to blitz the finale at full machine
speed with four fingers, then tap it again to hand control back to the human
style. Both buttons can be dragged anywhere on screen.

The tap speed and fixed-gap settings only apply to the machine style; the human
styles work out their own timings.
