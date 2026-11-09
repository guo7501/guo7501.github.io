# guo7501.github.io

Personal academic website of Zipeng (Cooper) Guo. Plain HTML, no build step.

## Update content
Everything is in `index.html`. Publications, teaching, and projects are ordinary HTML you can edit in place. Keep images in `assets/` as JPG or WebP, around 1600 px wide.

## Files
- `assets/Zipeng_Guo_CV.pdf` — linked from the CV buttons; replace it with your latest CV using the same file name.
- `assets/Zipeng_Guo_Teaching_Portfolio.pdf` — linked from the Teaching Portfolio button and from the Courses part of Teaching; replace it with a newer version using the same file name.
- `assets/zipeng-guo.jpg` — portrait.

## Hero map
- `assets/austin-map.webp` is a pre-rendered, tilted map of the City of Austin (streets from U.S. Census TIGER/Line, boundary from the City of Austin).
- The arcs are drawn live from the `FLOWS` data near the top of the script in `index.html` (ten parks and their top home block groups, from aggregated Advan mobility data). The `CAM` values must match the map image, so change them only together with a re-rendered map.

## Teaching Portfolio
The Teaching Portfolio button (`id="portfolioLink"`) opens `assets/Zipeng_Guo_Teaching_Portfolio.pdf`. The same file is linked twice in the Teaching section: the dark button under the three numbers (`.tport-top`) and the card after the courses (`.tport-card`). To link somewhere else, search `index.html` for `Zipeng_Guo_Teaching_Portfolio.pdf` and change every `href`.

## Email button
The Email button in the hero opens a small panel (`id="mailpanel"`) with the school and personal addresses, each with a Copy button. To change an address, edit both the text in `.mp-v` and the `data-copy` value of the button next to it. The panel is moved to the end of the page when it opens, so nothing on the page can cover it.

## Featuring
The steps 1–5 are written onto the workflow image (`assets/featuring-workflow.jpg`). Each step is one `<li class="fs">` in `.fsteps`; its `left`, `top`, and `width` place it under the image's own stage labels, so keep them if you only change the words. On narrow screens the steps move below the image and numbered pins (`.fpin`) mark the stages.

## New-paper bar
The thin bar above the navigation is the `<a class="ribbon">` element near the top of `index.html`. To announce a different paper, change its title, journal, and link. Delete the element to remove the bar.

## Icons
`favicon.svg`, `favicon-32.png`, and `apple-touch-icon.png` (home-screen icon on phones) sit next to `index.html`.

## Research list
Each paper in the Research section is one `<li data-t="...">` inside `#p-j` (journal articles) or `#p-c` (conference presentations), grouped by year with the newest year first.
`data-t` sets the topic: `value` (Park Visitation and Recreation Value), `design` (Design and Environment), `access` (Park Accessibility), `perf` (Green Infrastructure).
To add a paper, copy an existing `<li>` with the same topic, edit the text, and update the counts on the topic card and the tab.

## Teaching
- **Teaching photos** are `assets/teach-*.webp` (3:2, 1350 × 900). Each slide in `#tshow` is one `<div class="tslide">` holding the photo and an `<svg class="tfx">` with the hand-drawn lines on top, which are drawn in the photo's own 1350 × 900 space. Captions come from the `aria-label` of the matching button in `.tdots`, so edit the caption there. To add a photo, copy a slide and a button, then change the image, the caption, and the lines (or delete the lines inside `<svg>` for a plain photo).
- **Student comments** are the `<figure class="tcard">` cards inside the first `<div class="tset">`. The strip repeats that set three times so it never runs out on wide screens, so copy any change into the other two `tset` blocks as well. The dark card is the one with class `feat`.
- **Courses** has two columns in `.tcols`: *Courses I can teach* (groups of `<li>` in `.cgrp`) and *Teaching record* (rows of the table `.trec`, grouped as Graduate, Undergraduate, and Mentoring, newest first). The role label's class sets its color: `co` co-instructor, `ad` advisor, none for the others.
- The three numbers at the top of the section (courses, students, terms) are typed by hand and follow the teaching record without guest lectures and mentoring, so update them when you add a course.

## Community Projects (nav: Projects)
- The section has `id="practice"`, so old links still work. The nav label is "Projects".
- Each featured project is an `<article class="case">`: title, a status pill (`<p class="cstatus">`), a summary, and a `facts` list, followed by a `.deck`.
- A deck is a set of pages where the image and the text change together. Page *n* is made of three matching parts with the same order: a tab button in `.dtabs`, a `<figure class="dimg">` in `.dimgs`, and a `<div class="dtext">` in `.dtexts`. To add a page, copy one of each, give the tab and panel new ids (for example `cs-t6` and `cs-p6`), and remove `class="on"` and add `aria-hidden="true" inert` on the copies (only the first page is shown at load). Then update the page count in two places: `style="--n:6"` on the `.deck` (sets the tab widths) and `/ 06` in `.dcount`.
- Images that contain drawings with labels use `class="dimg contain"` so nothing is cut off; photos and renderings fill the frame.
- The featured projects, in order: Park Design Toolkit, Charlotte Sharp Children's Center Garden, Neal Cancer Center Therapeutic Rooftop Garden. The buttons under a project's summary are in `<p class="clinks">`.
- Images: `assets/pdt-*.webp` (Park Design Toolkit pages, made from the teaching portfolio, pp. 30–31), `assets/cscc-*.webp` (Charlotte Sharp Children's Center), and `assets/hm-*.webp` (Neal Cancer Center).
- Other projects are the `<li>` items in `.plist`.
