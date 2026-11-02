# guo7501.github.io

Personal academic website of Zipeng (Cooper) Guo. Plain HTML, no build step.

## Update content
Everything is in `index.html`. Publications, teaching, and projects are ordinary HTML lists you can edit in place.

## Replace a placeholder image
Practice and Research cards show a generated visit map until an image is added.
Put the image in `assets/`, then add an `<img>` inside that card's `<figure class="plate" ...>`:

```html
<figure class="plate" data-seed="4"><img src="assets/harrison-trail.jpg" alt="Harrison County trail plan"></figure>
```

Use JPGs around 1600 px wide (under ~400 KB each).

## Files
- `assets/Zipeng_Guo_CV.pdf` — linked from the CV buttons; replace it with your latest CV using the same file name.
- `assets/zipeng-guo.jpg` — portrait.

## Hero map
- `assets/austin-map.webp` is a pre-rendered, tilted map of the City of Austin (streets from U.S. Census TIGER/Line, boundary from the City of Austin).
- The arcs are drawn live from the `FLOWS` data near the top of the script in `index.html` (ten parks and their top home block groups, from aggregated Advan mobility data). The `CAM` values must match the map image, so change them only together with a re-rendered map.
