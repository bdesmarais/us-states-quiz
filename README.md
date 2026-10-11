# U.S. States Map Quiz

A self-quiz for placing the names of the 50 U.S. states on a map. Play it at **https://bdesmarais.github.io/us-states-quiz/**.

Click a state name to pick it up (click it again to put it down), then click a state on the map to place it. Click a placed state, or its name in the list, to take it back. The small Northeastern states also have boxes at the right edge you can click. **Submit** colors each state right (green), wrong (red) or blank (yellow), lists the right and wrong answers, and **Show correct map** labels every state.

A single static page (`index.html`) with D3 and topojson-client vendored in `vendor/`, along with the U.S. Census Bureau state boundaries from [us-atlas](https://github.com/topojson/us-atlas) (`states-albers-10m.json`, Albers projection with Alaska and Hawaii inset). No build step and no server code.

## Is the answer key right?

[verify.html](https://bdesmarais.github.io/us-states-quiz/verify.html) checks it against an independent source. For each state it projects the Census Bureau's official internal point (2024 Census Gazetteer, `data/census_gazetteer_2024_state_internal_points.json`) with the map's own Albers USA projection and confirms the point falls inside the shape labeled with that state's name and inside no other shape, and that each shape's FIPS code matches the Census code. All 50 pass.
