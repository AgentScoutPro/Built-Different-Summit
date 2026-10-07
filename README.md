# Built-Different-Summit

Landing page for The Built Different Summit, Friday, November 13, 2026, Mesa, AZ. Presented by Premier Inspector Group.

Static site, no build step: `index.html` plus `assets/`. Vercel serves the repo root as-is.

- Ticket buttons link to the Eventbrite listing with `?aff=landingpage` for tracking.
- The four background videos are scrubbed by scroll position. They are encoded with a keyframe every 4 frames so seeking stays smooth; re-encode replacements the same way (`ffmpeg -i in.mp4 -an -c:v libx264 -crf 28 -g 4 -bf 0 -pix_fmt yuv420p -movflags +faststart out.mp4`).
