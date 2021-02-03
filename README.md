# drafts

  [![license][license-image]][license-url]

A list of things to think about.

## A grid extension for laying out front-ends

🔧

* resizable rulers, semitransparent dashed lines
* separate grids attachable to selected DOM elements (via a context menu option)
* movable 0-points (negative numbers on the left/top)
* configurable offset patterns (for vertical rhythm)
* clickable colored cells (to draft high-level layout containers quickly)

See:

* [Super-Powered Grid Components with CSS Custom Properties](https://css-tricks.com/super-power-grid-components-with-css-custom-properties)

## An extension that tracks requests destinations

🔬

* collect number of requests made to different domains
* compare the current one (origin) to externals
* render various charts (with d3 utils)
* re-playable "live" reports (based on persistent logs)
* blockers comparison (draw milestones when some blocker got installed/removed)

## An extension that measures time spent in active browser tabs

🔬

* completely client-side (no requests triggered from the extension, no tracking)
* collect:
  * "start/finish" timeframes (in active tab)
  * times a URL is entered, together with navigation within the domain (path-level gradation)
* display a summary and trends to showcase patterns (how much time is spent with which website)
* filtering and whitelisting (if only certain domains are interesting)
* grouping (productive, social, news, etc.)

## Physical scrobbler

🎧

* a semi-automated scrobbler, connecting [Discogs](https://www.discogs.com/developers#page:database,header:database-search) and [Last.fm](https://www.last.fm/api/scrobbling) APIs
* user flow:
  1. find a record via a search box (by artist, album, catalog number, etc.) or select it from the personal collection
  1. choose which tracks to scrobble and which to skip, enter a starting time
  1. click "scrobble", check the status
  1. if the record is scrobbled for the first time, it could be added to the personal collection
  1. optionally edit the record in the collection, e.g. choose a particular release, add/remove tracks, add notes
* existing integrations: [Vinyl Scrobbler](https://vinylscrobbler.com/), [Open Scrobbler](https://github.com/elamperti/openwebscrobbler), [Universal Scrobbler](http://universalscrobbler.com/), [The Record Scrobbler](https://github.com/fptavares/scrobbler)

## JS lib to run migrations

🔧

* timestamp comparison
* runner: orchestration
* migration: setup, teardown, up, down, validate

## Functional strategy game

🎮

* units - actors
* each unit type is configured with some predefined set of aspects
* units influence each other
* groups could gravitate the others
* different kinds of units: heavy, dynamic, robust, resilient etc.
* colors represent reactive interconnections

## Personal/family budget tracker

📊

* define categories/subcategories
* log (consider sort of a biweekly calendar)
* plan (place predefined amounts and recurring payments)
* biweekly/monthly graphs to observe trends
* [Sankey diagrams](https://s.dou.ua/storage-files/sanky3.png) for yearly reports, consider [`d3-sankey`](https://github.com/d3/d3-sankey)

## "Social disconnector" - a web service that organizes chosen subscriptions

🔭

Like Feedly, but for social media.
The idea is to eliminate noise by reducing time spent on native feeds,
having a list of accounts/tags you could explore just like RSS feeds.
That implies a need to be authorized by corresponding providers.

See:

* [Awesome OSINT: Social Media Tools](https://github.com/jivoi/awesome-osint#social-media-tools)

## Pixel, turn-based game

🎮

* units: battleships (different in size and other params) and docks
* resources: money, steel and fuel (convertible), the more shore territories are controlled, the more resources their bring
* one game move - select (one or more ships), shift to another area (depends on available speed and fuel) and fire (a target needs to be defined) or skip
* ships are pre-selectable before the round starts and also could be built in docks
* damage depends on number and power of guns (sum of all guns on all selected ships)
* different guns have different effective areas, accuracy, damage power and (most importantly) - shell limits
* ships have armour that can be damaged (instantly) and repaired (if small - slowly during game moves, faster - in docks)
* a ship could be *captured* (either turned into an abandoned obstacle or refueled/recharged and became controlled), if it runs out of fuel or ammo
* a map is not fully visible - it's limited to areas close to player's ships and controlled shores
* damage is based on proximity - each shot looses precision with distance growing
* it's a multiplayer, but turn-based game (time limit is configurable) - every player defines a *move* and then all involved ships (of all players) execute those moves - they shift, fire, receive damage and eventually sink
* when ships of player A define a target among ships of player B, they should aim for the *upcoming* position of those B-ships, i.e. guessing a place where B would point the ships to
* number of players is not limited to 2, it starts from 1 (training mode with static targets) and can grow to some meaningful limit (e.g. 8)
* each turn is recorded, so rounds could be replayed

```
+-----------------------------------------------+
| +---\   +--\                                  |
| |●●●●>  |●●●>                      /---+      |
| +---/   +--/        ·····/---+    <○○○○|      |
|                 ····· ··<○○○○|     \---+      |
| +-+   +----\·····   ·····\---+                |
| |●|   5●●●●●>     ·····     +-+   /------+    |
| |●|   +----/    ·····       |○|  <○○○○○○○|    |
| |●|           ··· ··        |○|   \------+    |
| |●|    +3+  ···  ··         \○/               |
| \●/    |●|···   ··           ⌄                |
|  ⌄     |●|·    ··                             |
|        \●/  +-\·              /------+     ⌃  |
|         ⌄   2●●>             / ○○○○○○|    /○\ |
|             +-/             <○○○○○○○○|    |○| |
|                              \ ○○○○○○|    |○| |
| +--------\                    \------+    +-+ |
| |●●●●●●●●●\                                   |
| |●●●●●●●●●●>              +-----\             |
| |●●●●●●●●●/               |○○○○○○>            |
| +--------/                +-----/             |
+-----------------------------------------------+
```

## Pixel font

🎨

* some characters are already used, see examples below
* inspired by [Mogee Font](https://github.com/kuzminadya/mogeefont/)
* see ["A beautifully illustrated glossary of typographic terms you should know"](https://www.canva.com/learn/typography-terms/) for terminology

<details>
  <summary>Examples:</summary>

  <a href="https://avatars2.githubusercontent.com/u/48298354">
    <img
      src="https://avatars2.githubusercontent.com/u/48298354"
      width="115"
      alt="Minimalistic Games"
    />
  </a>

  <a href="https://avatars1.githubusercontent.com/u/48178221">
    <img
      src="https://avatars1.githubusercontent.com/u/48178221"
      width="115"
      alt="Music Stats"
    />
  </a>

  <a href="https://avatars1.githubusercontent.com/u/24212226">
    <img
      src="https://avatars1.githubusercontent.com/u/24212226"
      width="115"
      alt="Color Moose"
    />
  </a>
</details>

[license-image]: https://img.shields.io/github/license/oleksmarkh/drafts.svg?style=flat-square
[license-url]: https://github.com/oleksmarkh/drafts/blob/master/LICENSE
