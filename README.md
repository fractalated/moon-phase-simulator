# Moon Phase Orrery

An interactive lunar phase simulator for the classroom. Drag the Moon around its
orbit and watch the phase you would actually see from Earth change in step.

**[Open the simulator →](https://fractalated.github.io/moon-phase-orrery/)**

## What it does

- **Two linked views.** A top-down Sun–Earth–Moon diagram on the left, the
  naked-eye view of the disc on the right. Move one, the other follows.
- **A real terminator.** The lit shape is drawn as a true terminator ellipse
  over the near-side maria, not a stock crescent graphic, so the disc always
  matches the geometry beside it.
- **Scrub or play.** Drag the Moon, drag the slider, click any of the eight
  phase positions, or play a full synodic month in about 22 seconds.
- **Opens on tonight's moon.** The page loads at the current phase.
- **Hemisphere toggle.** Switching to Southern rotates the whole view 180°,
  maria included — a waxing crescent is lit on the left down there.
- **Readouts.** Illuminated fraction, moon age, elongation, moonrise and
  moonset — enough to show that a first quarter moon rises at noon.

## Misconceptions it is built to address

1. Phases are not Earth's shadow. Half the Moon is always lit; a phase is how
   much of that lit half is turned toward us.
2. There is no permanently dark side. The same face points at us, but sunlight
   sweeps across it — every spot gets about 14.8 days of day and 14.8 of night.
3. Daytime moons are normal. Only the full moon rises at sunset and sets at
   sunrise.

## Accuracy, honestly

The geometry is exact; the distances and sizes are not to scale. Two
deliberate simplifications:

- **Rise and set times** use the classroom approximation — new moon rises at
  06:00, everything else about 50 minutes later per day — not a real ephemeris,
  and no correction for latitude or time of year.
- **"Today's moon"** is computed from a mean synodic month (29.530588853 days)
  counted from the new moon of 6 January 2000, so it can be off by a few hours.
  Near new or full that is visible; mid-phase it is not.

For precise phase, libration and distance, use NASA's Dial-a-Moon:
<https://svs.gsfc.nasa.gov/5587/>

## Running it

One file, no build step, no dependencies. Open `index.html`, or:

```bash
python3 -m http.server 8000
```

The only network request is a Google Fonts stylesheet; the page falls back to
system fonts without it.

## License

MIT — see [LICENSE](LICENSE). Use it in your classroom, fork it, rewrite it.
