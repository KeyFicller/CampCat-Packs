## Pitfalls
- A view that still shows the page's own chrome (bottom tabs, resource bar, 招募) is that page with something selected, not a new page; a second anchor there makes every locate ambiguous.
- Cropping a round icon together with the coordinate label under it breaks matching when that label's text changes; cut the icon's disc alone.
- With a saved login the launcher/entry hop lands straight on the map, so the title-screen template times out; goto the login anchor instead.
- `save_template`'s self-check hands back a corrected region when a box clips a round rim or drags the plate under glyphs in; resave with the given region.
- Consecutive `view_crop` calls are capped at about three; look once per element, then save the template.
- Tapping terrain to dismiss a panel can open a different screen (it hit 招募 here); leave the screen by a known control.