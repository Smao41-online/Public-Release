# 🪐 Board Game Galaxy

A board game collection as a phone app — **720 games and 15 on the wishlist**, laid
out as a solar system. Browse it, search it, scan a box in a shop to see whether it
is already there, or let it pick something for tonight.

This is a **snapshot**, taken on **15 November 2026**. It is a complete, self-contained
copy: the app reads no database, needs no account and sends nothing anywhere.

## Install it

Open **<https://smao41-online.github.io/Public-Release/board-game-galaxy/>** on your
phone, then:

| | |
|---|---|
| **iPhone / iPad** | In **Safari**: Share → **Add to Home Screen** → Add |
| **Android** | In **Chrome**: ⋮ → **Install app** / *Add to Home screen* |

It then opens full screen with its own icon, starts instantly and works with no
signal at all. Nothing is installed from an app store and there is nothing to update.

> On iPhone it has to be **Safari** — Chrome on iOS cannot add a web app to the home
> screen. You can of course just use it in the browser tab without installing.

It also runs fine on a desktop browser; the page simply stays phone-shaped.

## What it does

| Tab | |
|---|---|
| 🪐 **Galaxy** | The whole collection as planets. Search hits the English title, the Czech title and the BoardGameGeek name at once; filter by language or player count; sort by rating, year or weight. Tap a planet for the full page — rating, players, play time, weight, year, designers, categories — and step through the collection from there with ‹ ›. |
| 📷 **Scan** | Point the camera at a barcode. If that box is in the collection you get **✓ owned**, if it is on the wishlist **✦ wishlist**, otherwise **✕ not in the collection**. Useful standing in a shop. |
| 🎲 **Tonight** | Say how many players, how long you have, what kind of game and how heavy — it suggests what fits, best rated first, and prints the criteria it used above the results. |

Any game page has **↗ Share this game**, which hands the title, rating and link to
whatever you normally share with.

## Make it work with no signal

Tap **ⓘ** at the top, then **⬇️ Save the pictures for offline**. It downloads all
698 box pictures — about 8.5 MB, so do it on wi-fi — and from then on the app opens
with no connection at all, pictures included. It can be stopped and restarted, and
never fetches a picture it already has.

Without that step the collection, search and scanning still work offline; only the
box art needs a connection, and anything missing is drawn as a planet instead.

## What it deliberately does not do

It is read-only. There is no adding, editing, removing or publishing — those live in
the private tool this snapshot was exported from. Personal notes are not included.

## Good to know

- **Box art comes from BoardGameGeek's public image servers** when you are online,
  and is kept on the phone once seen. Offline, or if an image is missing, each game
  is drawn as its own coloured planet instead — nothing breaks.
- **The barcode scanner needs `https`**, which the install link above is. Opening the
  files from a disk (`file://…`) lets you browse everything but the camera will not
  start, and neither will the home-screen install.
- **Barcodes only come back ✓ owned if that box has been scanned before** on the
  private side — the collection is mostly Czech editions, which no public barcode
  database covers properly. Unknown ones say so plainly rather than guess.
- **Ratings, weights and play times are BoardGameGeek's**, as of the snapshot date.

## Getting a newer snapshot

The app is replaced from time to time with a fresh export, at the same address — so
the link you were sent keeps working and simply shows more games. If you installed it
to the home screen, it picks the new copy up by itself the next time you open it with
a connection.

Each snapshot is also attached to a release here as a zip, if you would rather keep
one: unzip it and open `index.html` in a browser. Browsing works; the camera does not,
for the reason above.
