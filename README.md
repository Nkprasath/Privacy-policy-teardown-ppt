# Privacy Policy Teardown

A presentation deck for a live webinar on what public privacy notices actually promise,
run jointly by Privacy Labs and Businezexcellence.

**Live deck: https://nkprasath.github.io/Privacy-policy-teardown-ppt/**

## What this is

One self-contained HTML file. `index.html` is the entire deck: 19 slides, 33 reveal steps.
Photos and both logos are embedded as data URIs, so there are no image files to keep
alongside it. The only external dependencies are two libraries loaded from a CDN at runtime:

- [Rough.js](https://roughjs.com) for every hand-drawn mark: circles, boxes, arrows, ticks, crosses
- [Anime.js v4](https://animejs.com) for motion

That means the deck needs a network connection the first time it loads. Once loaded it
will keep running offline for the rest of the session.

## Presenting

Open the link above, press `F` for fullscreen, and share that browser tab.

| Key | Action |
|---|---|
| `→` `↓` `Space` | Next step, then next slide |
| `←` `↑` | Previous step, then previous slide |
| `Home` / `End` | First / last slide |
| `F` | Fullscreen |
| `N` | Presenter notes for the current slide |
| `Esc` | Close notes, then exit fullscreen |

The stage is a fixed 1920x1080 that scales to fit any window, so it holds up on a
projector or a laptop screen without reflowing.

## Editing during the session

Several fields are editable directly in the browser. Click and type:

- `[DATE]` on the title, sessions and group slides
- The three worst-finding lines on "Three sectors, three broken boxes"
- The six session titles on "Six sessions, same method"
- Speaker roles, contact addresses, group member count

Edits live in that browser tab only. They are not saved back to the file, so anything
you want to keep has to go into `index.html`.

## Still to fill in

- Both QR placeholders: one points at the compliance scanner on theprivacylabs.com,
  the other at the WhatsApp group invite
- The three worst-finding lines, after the actual scans are run
- Session dates

## Editing the file

Everything is in `index.html`: styles in the `<style>` block, slides as
`<section class="slide">` elements, and the per-slide choreography in the `plays` object
near the bottom of the module script. Each slide declares its own reveal count with
`data-steps` and its speaker note with `data-notes`.

To swap a photo, replace the `src` on its `<img>` inside `.spk .photo`. To swap a logo,
replace the `src` on the matching `<img class="logo">`. Both accept a data URI or an
ordinary relative path to a file committed next to `index.html`.

## A note on the teardown subjects

The three sites examined in the session are presented by sector, never by name.
Naming real companies while calling their policies non-compliant is a fight worth
avoiding, and the audience learns the same lesson either way.
