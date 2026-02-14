# AutoCrop Anniversary

Created by Zev based off a fork of [AutoCrop by Chromie](https://www.curseforge.com/wow/addons/autocrop) updated for WoW Classic Anniversary Edition.

## What it does

AutoCrop automatically equips your Riding Crop (and other riding gear) when you mount up, and swaps back to your normal gear when you dismount. It also supports:

- **Carrot on a Stick** + legacy enchanted gloves/boots (legacy mode)
- **Charm of Swift Flight** for druids in flight form
- **Engineering Goggles** auto-swap in Outland gas cloud zones
- **Azure Silk Belt** auto-swap while swimming
- PvP battleground support
- **Draggable button** — toggle the addon on/off with a minimap-style button (Alt+drag to reposition)
- **Instance detection** — automatically unequips riding gear when entering instances
- **Combat safety** — never swaps gear during combat

## Changes from original

- Updated bag API calls (`GetContainerNumSlots`, `GetContainerItemLink`, `GetContainerItemID`) to the `C_Container` namespace required by the Anniversary client
- Updated `## Interface` version to `50503` for TBC Anniversary Classic compatibility
- Renamed TOC file to match `AutoCrop-Anniversary` folder name
- Fixed global variable leaks that could conflict with other addons
- Fixed `esMX` locale using incorrect Portuguese zone names instead of Spanish
- Added English locale fallback for unsupported languages
- Fixed button scale being stored as a string instead of a number
- Fixed operator precedence bug in button scale display
- Fixed `/ac slot` help text always showing "1" instead of the actual slot number
- Fixed spelling of "avaliable" to "available"
- Added OnUpdate throttle to reduce CPU usage
- Fixed ADDON_LOADED handler running locale setup and state resets for every addon instead of only for AutoCrop
- Removed redundant `AutoCropSearchInventory` call on load (already called inside `AutoCropOnLoad`)
- Removed unused `AutoCropFindBuff` function and dead local variables
- Removed unhandled `PLAYER_LOGIN` event registration

## Supported Riding Trinkets

- Riding Crop (25653)
- Skybreaker Whip (32863)
- Skybreaker Whip — flight form variant (32481)

## Slash Commands

Use `/autocrop` or `/ac` followed by:

| Command | Values | Description |
|---------|--------|-------------|
| `enable` | `0` / `1` / `toggle` | Enable or disable the addon |
| `slot` | `13` / `14` | Choose upper or lower trinket slot |
| `goggles` | `0` / `1` | Toggle engineering goggles auto-equip |
| `pvp` | `0` / `1` | Toggle riding gear in battlegrounds |
| `swimming` | `0` / `1` | Toggle Azure Silk Belt when swimming |
| `legacy` | `0` / `1` | Toggle between TBC and Classic riding gear |
| `button` | `0` / `1` / `reset` / `scale <n>` | Show/hide/reset the button, or set its scale |
| `reset` | | Reset all saved settings (reload UI after) |

Running `/ac` with no arguments prints all commands and their current values.

## Installation

Place the `AutoCrop-Anniversary` folder inside your `Interface\AddOns\` directory:

```
World of Warcraft\_anniversary_\Interface\AddOns\AutoCrop-Anniversary\
```

## Credits

Original addon by **Chromie** (Nethergarde Keep) - [CurseForge page](https://www.curseforge.com/wow/addons/autocrop)

Anniversary edition by **Zev**
