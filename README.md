# Days of the Week

[![🧪 Tested On](https://img.shields.io/badge/🧪%20Tested%20On-A20.6%20b9-blue.svg)](https://7daystodie.com/) [![📦 Automated Release](https://github.com/jonathan-robertson/days-of-the-week/actions/workflows/release.yml/badge.svg)](https://github.com/jonathan-robertson/days-of-the-week/actions/workflows/release.yml)

- [Days of the Week](#days-of-the-week)
  - [Summary](#summary)
    - [Adjustments](#adjustments)
  - [Sister Project](#sister-project)
  - [Compatibility](#compatibility)
  - [Acknowledgement](#acknowledgement)

## Summary

7 Days to Die mod: Replace days count in UI with a day of the week.

The general idea is that the total day count is relatively meaningless to most players. Most players want to know what the day *means* for them and the recurring question many admins receive on a regular basis is "how many days till blood moon?"

If you use this mod, you'll be able to say "it happens every Sunday". No math. No second-guessing. Just simple.

> ℹ️ This mod does not alter the actual days within a game or server (many components in the game rely on server/world time increasing); it simply updates how the days are presented within the UI.

### Adjustments

Element | Change
--- | ---
Compass | Days replaced with day of the week
Journal | Day read is removed
Map | Day/Time entry is removed

## Sister Project

This mod is designed to work well with another if you're using a dedicated server: [Only Seven Days](https://github.com/jonathan-robertson/only-seven-days).

## Compatibility

Environment | Compatible | Does EAC Need to be Disabled? | Who needs to install?
--- | --- | --- | ---
Dedicated Server | Yes | No | only server
Peer-to-Peer Hosting | Yes | No | only the host
Single Player | Yes | No | self (of course)

## Acknowledgement

This mod as it's currently written is only possible due to the brilliant efforts of another modder and his willingness to share what he learned:

**Shado47** developed the [Immersive Days](https://7daystodiemods.com/immersive-days-display/) mod that "Changes the day counter below the compass to go through weekdays, months, and years. Starts on January 1st, 2020".

If this sounds even better to you than this mod does, I would highly encourage you to check out Immersive Days.
> ℹ️ Just like this mod, his does not require EAC to be disabled and is able to be served from a server without any client-side downloads.
