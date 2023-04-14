# Days of the Week

[![🧪 Tested On](https://img.shields.io/badge/🧪%20Tested%20On-A20.6%20b9-blue.svg)](https://7daystodie.com/) [![📦 Automated Release](https://github.com/jonathan-robertson/days-of-the-week/actions/workflows/release.yml/badge.svg)](https://github.com/jonathan-robertson/days-of-the-week/actions/workflows/release.yml)

- [Days of the Week](#days-of-the-week)
  - [Summary](#summary)
    - [Optional Vending Expiration Clock](#optional-vending-expiration-clock)
    - [Optional Trader Restock Clock](#optional-trader-restock-clock)
    - [Days Remaining Compatibility Mode](#days-remaining-compatibility-mode)
    - [Optional Short Day](#optional-short-day)
  - [Sister Projects](#sister-projects)
  - [Compatibility](#compatibility)
  - [Acknowledgements](#acknowledgements)

## Summary

7 Days to Die mod: Replace days count in UI with a day of the week.

> 🗺️ This mod is fully localized 🎉

The general idea is that the total day count is relatively meaningless to most players. Most players want to know what the day *means* for them and the recurring question many admins receive on a regular basis is "how many days till blood moon?"

If you use this mod, you'll be able to say "it happens every Sunday". No math. No second-guessing. Just simple.

> ℹ️ This mod does not alter the actual days within a game or server (many components in the game rely on server/world time increasing); it simply updates how the days are presented within the UI.

Element | Change
--- | ---
Compass | Days replaced with day of the week
Journal | Day read is removed
Map | Day/Time entry is removed
Quests | Date Completed is removed
Trader | Restock Date is removed (by default; see [Optional Vending Expiration Clock](#optional-vending-expiration-clock))
Vending | Date/Time Clock is added to Rentable Vending for Expiration Date reference (by default; see [Optional Trader Restock Clock](#optional-trader-restock-clock))

### Optional Vending Expiration Clock

Because the default Rentable Vending Machines present a *target* expiration date rather than the count for the number of days remaining before machine expiration, having a reference to the current game/server day is necessary for context.

One has been included in the "Product Name" column for this very purpose, but you can disable this by swapping `Config/windows.xml` with `Config/windows-remove-vend-clock.xml`.

### Optional Trader Restock Clock

Trader Restock Day is similarly referring to the day the trader expects to restock inventory; without knowing the current day, the context for this information is completely lost.

While the same kind of Date/Time clock *can* be added for traders with a Restock Day displayed, I decided to not include this by default and instead completely remove Restock Days from the Trader UI. I did this because Restock Days provides information that is not critically necessary for the player.

If you highly prefer to have Restock Days display, I have included an optional configuration that will add it back and include a Clock showing the current Day/Time. You can enable this by swapping `Config/windows.xml` with `Config/windows-add-restock-clock.xml`.

> ℹ️ If you do not like this, feel free to adjust

### Days Remaining Compatibility Mode

TODO

### Optional Short Day

If you want to integrate this mod into any existing mod, you can still use the same format found in line 3 of `windows.xml` to update your own compass days value.

> 🗺️ These optional short-dates are currently only available in English.

```xml
[{daycolor}]{# localization('dayOfTheWeek' + (day-1)%7)}[-] {time}
```

As a bonus, I've included short days as well - in case you're shooting for a more compact look:

```xml
[{daycolor}]{# localization('shortDayOfTheWeek' + (day-1)%7)}[-] {time}
```

## Sister Projects

This mod is designed to work well with a few others if you're using a dedicated server:

- [Only Seven Days](https://github.com/jonathan-robertson/only-seven-days)
- [Days Remaining](https://github.com/jonathan-robertson/days-remaining)

## Compatibility

Environment | Compatible | Does EAC Need to be Disabled? | Who needs to install?
--- | --- | --- | ---
Dedicated Server | Yes | No | only server
Peer-to-Peer Hosting | Yes | No | only the host
Single Player | Yes | No | self (of course)

## Acknowledgements

This mod as it's currently written is only possible due to the brilliant efforts of another modder and his willingness to share what he learned:

**Shado47** developed the [Immersive Days](https://7daystodiemods.com/immersive-days-display/) mod that "Changes the day counter below the compass to go through weekdays, months, and years. Starts on January 1st, 2020".

If this sounds even better to you than this mod does, I would highly encourage you to check out Immersive Days.
> ℹ️ Just like this mod, his does not require EAC to be disabled and is able to be served from a server without any client-side downloads.
