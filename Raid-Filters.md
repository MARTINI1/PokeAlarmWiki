## Overview

* [Prerequisities](#prerequisites)
* [Introduction](#introduction)
* [Parameters](#parameters)

## Prerequisites
This page assumes:

1. You have a working scanner.
2. You are familiar with
[JSON formatting](https://www.w3schools.com/js/js_json_intro.asp).
3. You are using the latest version of PokeAlarm.
4. You have read and understood the [Filters Overview](filters_overview)
page.

## Introduction

The `"raids"` section has three distinct settings.

| Setting Name         | Description                                   |
| -------------------- |---------------------------------------------- |
| enabled              | Process Raid Events only if `true`         |
| defaults             | See [filters](fitlers#defaults) page on defaults|
| filters              | See below parameters                           |

## Parameters

Raid Filters can use the following parameters to filter Raid Events:

| Parameter   | Description                                  | Example |
| ----------- |--------------------------------------------- |---------|
| quick_moves | Accepted quick moves, by id or name.         | `[ "Vine Whip", "Tackle"]` |
| charge_moves | Accepted charge moves, by id or name.       | `[ "Sludge Bomb", "Seed Bomb"]` |
| monsters    | Array of allowed monsters, by id or name.    | `[ "Raikou", "244", 245 ]`|
| min_raid_lvl | Minimum level of the egg.                | `0`     |
| max_raid_lvl | Maximum level of the egg.                | `5`    |
| current_teams | List of allowed current teams, by id or name. | `[ "Instinct", "Mystic" ]` |
| min_dist    | Min distance of event from set location in miles or meters (depending on settings). | `0.0` *|
| max_dist    | Max distance of event from set location in miles or meters (depending on settings). | `1000.0` *|
| gym_name_contains | List of regex's required to be in the gym name.  | `[ "Sponsored" , "West\\sOak"]` |
| geofences   | See [filters](fitlers#defaults) page on 'Geofences'    | `[ "geofence1", "geofence2" ]` |
| custom_dts  | See [filters](fitlers#defaults) page on 'Custom DTS'   | `{ "dts1" : "substitution" }` |
| is_missing_info | See [filters](fitlers#defaults) page on 'Missing Info' | `true` or `false` |

\* Floats can use `"inf"` to represent infinity