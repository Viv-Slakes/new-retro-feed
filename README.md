# New Retro — Contributing Entries

Games are listed in `feed.xml`. To add a game, copy the `<item>` block from `sample.xml` and fill it in. Lists with already existing values for Platform and Genres can be found at [platform.md](platform.md) and [genres.md](genres.md)

---

# Rules

## If you are found breaking any of the rules detailed below your additions might be partially or fully removed and you will be barred from expanding on the list.

## Games

- You are allowed to add games where at least one of the platforms it has been released for has been discontinued and the game has been published after the platform has been discontinued. Meaning: no more official game releases and any official online store closed down (e.g. 3DS). **IMPORTANT: Emulators are not platforms. If a release is not for the default UI of a platform it needs to be mentioned as part of the platform. (e.g. "3DS Homebrew-Launcher" instead of "3DS")**
- You are not allowed to add any games that communicate any kind of hateful message (e.g transphobia, queerphobia, racism).

## Opinions

- Your opinions are not allowed to communicate any kind of hateful message (e.g. transphobia, queerphobia, racism).
- Since opinions are meant to be interpreted as short reviews developers and people directly financially connected to a game are not allowed to provide their opinion. **IMPORTANT: People that fall in this Category are of course still welcome to add a game itself, just not an opinion.**


# Explanations for individual fields
## Required fields

### Title and identifier

```xml
<guid>Full Game Title Here</guid>
<title>Full Game Title Here</title>
```

Both should contain the game's full name, spelled identically. The `<guid>` is the unique identifier for the entry — no two games in the feed can share the same value.

### Link

```xml
<link>https://example.com/game</link>
```

The URL for the game's store page, itch.io listing, or official site.

### Developer / publisher

```xml
<dc:creator>Developer Name</dc:creator>
```

The name of the developer or publisher. For games with multiple creators, separate names with a comma:

```xml
<dc:creator>Studio One, Studio Two</dc:creator>
```

### Description

```xml
<p>A short description of the game.</p>
```

A short description of the game. If available an official description works best. This must be a plain `<p>` tag with no class.

### Platforms

```xml
<h2>Platforms</h2>
<ul class="platforms">
  <li>Game Boy</li>
  <li>Analogue Pocket</li>
</ul>
```

Which systems the game runs on. Any discontinued system or modernised equivalent is fair game (Game Boy, Game Boy Color, Game Boy Advance, Game Boy Advance SP, ModRetro Chromatic, Analogue Pocket, Browser, etc.). Use consistent spelling across entries so the platform filter groups them correctly.

### Genres

```xml
<h2>Genres</h2>
<ul class="genres">
  <li>Platformer</li>
  <li>Adventure</li>
</ul>
```

One or more genre tags. Use consistent spelling across entries so the genre filter groups them correctly. Use `TBD` if the genre hasn't been determined yet.

### Release

```xml
<h2>Release</h2>
<ul class="release">
  <li>Digital</li>
</ul>
```

How the game is available. Accepted values are `Digital` and `Physical`. Include both if the game has both a digital and a physical release.

---

## Optional fields

These can be omitted entirely if not applicable.

### Opinion

```xml
<h2>Opinion</h2>
<p class="opinion" data-author="Your Name">Your opinion goes here.</p>
```

A short write-up about the game. The `data-author` attribute is optional but strongly encouraged so readers know who wrote it.

Multiple contributors can each add their own opinion to the same entry by including additional `<p class="opinion">` elements:

```xml
<h2>Opinion</h2>
<p class="opinion" data-author="First Person">First opinion here.</p>
<p class="opinion" data-author="Second Person">Second opinion here.</p>
```
