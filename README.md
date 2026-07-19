# Deutschlandticket Adoption Potential — J&J Medical GmbH, Norderstedt

This project looks at how convenient public transport is for employees traveling
to Johnson & Johnson Medical GmbH in Norderstedt, and estimates how many of them
would likely switch to using the Deutschlandticket if it were offered.

## What this does

1. Since real employee addresses can't be used, we created 600 made-up (synthetic)
   home locations spread across 12 areas in and around Hamburg.
2. We mapped out the nearby public transport network — the U1 and S1 subway/train
   lines and the AKN regional train — including how often trains run on each.
3. For each synthetic employee, we calculated their full door-to-door travel time:
   walking to the nearest station, waiting for a train, riding it, changing trains
   if needed, and walking to the office at the end.
4. We grouped everyone into four time bands: 30 minutes or less, 31-45 minutes,
   46-60 minutes, and over 60 minutes.
5. We gave each employee a "likelihood to adopt the Deutschlandticket" score out
   of 100, based on: how long their commute is, how good their connection is
   (frequent trains, no changes needed), how close they live to a station, and
   whether public transport is about as fast as driving would be.
6. We summarized all of this into an easy-to-read report: what percentage of
   employees fall into each travel-time band, how many are likely to adopt the
   ticket, which areas have the best and worst public transport access, and what
   factors matter most.

## Interactive map

There's also an interactive map, but a quick heads-up: if you open the notebook
directly on GitHub, the map will look blank. That's just a GitHub limitation —
its notebook viewer doesn't run the map's code.

To see the actual working map, click here instead:
👉  https://-jnj-deutschlandticket-commute-analysis/

On the map, you can see:
- Where each synthetic employee "lives," color-coded by how likely they are to
  adopt the ticket (red = unlikely, yellow = maybe, green = likely)
- The J&J office location
- Nearby train and subway stations
- A heatmap layer you can turn on to see adoption potential at a glance

(If you'd rather see the map appear directly inside the notebook, just open
`JnJ_Commute_Analysis.ipynb` in Google Colab or Jupyter and run it there.)

## A note on how accurate this is

Travel times in this project are estimated using distances and known train
schedules — not a live route planner (since this project didn't have access to
one). It's a solid stand-in for this kind of analysis, but if this were used for
a real decision, the next step would be plugging in an actual public transport
routing service (like HVV's own journey planner) for more precise numbers.
