# crazy-ideas

  [![license][license-image]][license-url]

A list of things to think about.

## A grid extension for laying out front-ends

:wrench:

There might be many similar ones out there, and you don't need an extension to simply measure distance
(macOS: `⌘`+`⇧`+`4` followed by `ESC` without releasing a mouse).
But I dare to guess that there might not be an almost UI-less one that just shows a semitransparent resizable grid.

See:

* [Super-Powered Grid Components with CSS Custom Properties](https://css-tricks.com/super-power-grid-components-with-css-custom-properties)

## An extension that tracks requests destinations

:microscope:

* collect number of requests made to different domains
* compare the current one (origin) to externals
* render various charts (with d3 utils)
* re-playable "live" reports (based on persistent logs)
* blockers comparison (draw milestones when some blocker got installed/removed)

## An extension that measures time spent in active browser tabs

:microscope:

* completely client-side (no requests triggered from the extension, no tracking)
* collect:
  * "start/finish" timeframes (in active tab)
  * times a URL is entered, together with navigation within the domain (path-level gradation)
* display a summary and trends to showcase patterns (how much time is spent with which website)
* filtering and whitelisting (if only certain domains are interesting)
* grouping (productive, social, news, etc.)

## JS lib to run migrations

:wrench:

* timestamp comparison
* runner: orchestration
* migration: setup, teardown, up, down, validate

## Functional strategy game

:video_game:

* units - actors
* each unit type is configured with some predefined set of aspects
* units influence each other
* groups could gravitate the others
* different kinds of units: heavy, dynamic, robust, resilient etc.
* colors represent reactive interconnections

## Personal/family budget tracker

:bar_chart:

* define categories/subcategories and tags
* log
* plan (including recurring payments)
* stats (diagrams)

## "Social disconnector" - a web service that organizes chosen subscriptions

:telescope:

Like Feedly, but for social media.
The idea is to eliminate noise by reducing time spent on native feeds,
having a list of accounts/tags you could explore just like RSS feeds.
That implies a need to be authorized by corresponding providers.

See:

* https://github.com/jivoi/awesome-osint#social-media-tools

## Pixel, turn-based game

:video_game:

* units - battleships (different in size and other params)
* one game move - select (one or more ships), shift to another area and fire (a target needs to be defined)
* damage depends on number and power of guns (sum of all guns on all selected ships)
* different guns have different effective areas, accuracy, damage power and (most importantly) - bullet limits
* ships have armour that can be damaged (instantly) and repaired (granularly, during game moves)
* each ship, gun and bullet costs something, depending on corresponding params
* it's a multiplayer, but turn-based game - during each round every player defines a *move* and then all involved ships (of all players) execute those moves - they shift, fire, receive damage and eventually sink
* when ships of player A define a target among ships of player B, they should aim for the *upcoming* position of those B-ships, i.e. guessing a place where B would point the ships to
* number of players is not limited to 2, it starts from 1 (training mode with static targets) and can grow to some meaningful limit (e.g. 8)
* each turn is recorded, so after the battle the whole sequence could be restored as animated scene

```
+-----------------------------------------------+
| +---\   +--\                                  |
| |●●●●>  |●●●>                      /---+      |
| +---/   +--/         ····/---+    <○○○○|      |
|                 ····· ··<○○○○|     \---+      |
| +-+   +----\····    ·····\---+                |
| |●|   5●●●●●>     ·····     +-+   /------+    |
| |●|   +----/    ·····       |○|  <○○○○○○○|    |
| |●|           ··· ··        |○|   \------+    |
| |●|    +3+  ···  ··         \○/               |
| \●/    |●|···   ··           ⌄                |
|  ⌄     |●|     ··                             |
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

## A map with annotated bicycle routes

:earth_africa: :bicyclist:

* export routes from Strava and/or other sources
* an editor that enables custom annotations (left turns, traffic lights, trams, etc.)
* a map to display the routes
* sharable links (profiles, routes, selected areas)
* public profiles should be protected by a clear policy
* support for private segments
* replayable rides as videos/gifs (if imported data has timestamps for segments)

## Pixel font

:art:

* some characters are already used, see examples below
* inspired by [Mogee Font](https://github.com/kuzminadya/mogeefont/)
* see ["A beautifully illustrated glossary of typographic terms you should know"](https://www.canva.com/learn/typography-terms/) for terminology

Examples:

<a href="https://github.com/music-stats">
  <img
    src="https://avatars1.githubusercontent.com/u/48178221"
    width="115"
    alt="Music Stats"
  />
</a>

<a href="https://github.com/color-moose">
  <img
    src="https://avatars1.githubusercontent.com/u/24212226"
    width="115"
    alt="Color Moose"
  />
</a>

<a href="https://github.com/jam-keeper">
  <img
    src="https://avatars2.githubusercontent.com/u/46428378"
    width="115"
    alt="Jam Keeper"
  />
</a>

[license-image]: https://img.shields.io/github/license/oleksmarkh/crazy-ideas.svg?style=flat-square
[license-url]: https://github.com/oleksmarkh/crazy-ideas/blob/master/LICENSE
