# Abdul Wassay & Warisha · Walima Invitation

A static website. No build step, no dependencies. Same hosting as the wedding invitation (GitHub + Vercel).

| File | What it is |
|---|---|
| `index.html` | The whole invitation: the living lake, the swans, the letter, the lotus, the pearl shells, the details, the lamps of dua |
| `assets/sky.jpg` | The turquoise marble sky |
| `assets/sprites.webp`, `assets/sprites.png` | The crowned swans, gold flowers and lotus blossoms (PNG is the fallback for older phones) |
| `assets/fonts/` | The typefaces, stored with the site so they load fast everywhere |
| `walima.ics` | Calendar file iPhones open from the "Add to Calendar" button |
| `vercel.json` | Tells Vercel to send `walima.ics` as a calendar file |
| `og.jpg` | The preview picture WhatsApp and Facebook show when the link is shared |
| `favicon.png`, `apple-touch-icon.png` | Browser tab and home-screen icons |

## Put it online (GitHub + Vercel)

1. Create a new GitHub repository and upload **everything in this folder** (keep the `assets` folder as it is).
2. In Vercel choose **Add New → Project** and import that repository.
3. Set **Framework Preset** to **Other**. Leave the build command empty and the output directory as the root.
4. Press **Deploy**. Every later push to GitHub updates the live site automatically.

## Before sending to guests

**1. Your live address.** The preview tags in `index.html` point to
`https://walima-wassay-warisha.vercel.app`. If Vercel gives you a different address, search `index.html`
for `walima-wassay-warisha.vercel.app` and replace all of them with your real address.
WhatsApp only shows the preview picture when this address is correct.

**2. The venue pin.** The "Open in Maps" button searches for *Karsaz Service Road, Karachi*. For an exact pin,
open the hall in Google Maps → **Share → Copy link**, then in `index.html` replace the value of `MAP_URL`
with that link (keep the quotes).

## Personal links for each guest

Add the guest's name to the end of the link. The cover will say "Specially for …", the folded letter
carries their name, and the opened letter begins "Dear …,".

- `https://your-address/?to=Ahmed Family`
- `https://your-address/#Ahmed-Family`

## How the experience flows

1. **The lake** – guests touch the water; two crowned swans glide in and form a heart, the names are written in gold.
2. **The letter** – a sealed, folded letter; tapping the wax seal unfolds it (it tilts and shimmers under the finger).
3. **The verse** – press and hold the lotus; it blooms and reveals Surah Ar-Rum 30:21.
4. **Save the date** – three pearl shells open to 13 · 12 · 2026, followed by a live countdown.
5. **The evening** – gathering 9:00 pm, dinner 10:00 pm, Karsaz Service Road, with map and calendar buttons.
6. **Duas** – every tap on the water floats a little lamp carrying the guest's dua.
7. **With love** – from Muhammad Sulieman & Mansha Sulieman and family, with a replay button.

A little golden bird at the bottom always says what to do next, and the round gold arrow moves on
(if a guest skips a step, the arrow reveals it for them first, so nobody misses the details).
Swiping up/down, the arrow keys and the mouse wheel also turn the pages.

## Good to know

- The music is an original gentle waltz generated live by the page, so there is no audio file to host.
  It starts when the guest first touches the water; the round button at the top right pauses it.
  On iPhones the silent switch mutes it.
- The page lowers its own visual detail on slower phones automatically, and respects the
  "Reduce motion" setting on iPhone and Android.
- WhatsApp remembers a link's preview. If you shared the link before the preview was right,
  test with a fresh variant such as `?to=Test`.
- All dates and times live in the `CFG` block at the top of the script in `index.html`
  (written in UTC: 9:00 pm in Pakistan is 16:00 UTC). If the time changes, also update `walima.ics`.
