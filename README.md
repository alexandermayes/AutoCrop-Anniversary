# AutoCrop Anniversary

A fork of [AutoCrop by Chromie](https://www.curseforge.com/wow/addons/autocrop) updated for WoW Classic Anniversary Edition.

## What it does

AutoCrop automatically equips your Riding Crop (and other riding gear) when you mount up, and swaps back to your normal gear when you dismount. It also supports:

- **Carrot on a Stick** + legacy enchanted gloves/boots (legacy mode)
- **Charm of Swift Flight** for druids in flight form
- **Engineering Goggles** auto-swap in Outland gas cloud zones
- **Azure Silk Belt** auto-swap while swimming
- PvP battleground support

## Changes from original

- Updated bag API calls (`GetContainerNumSlots`, `GetContainerItemLink`, `GetContainerItemID`) to the `C_Container` namespace required by the Anniversary client
- Updated `## Interface` version to `11508` for Anniversary Classic compatibility

## Slash commands

| Command | Description |
|---------|-------------|
| `/ac` or `/autocrop` | Show all commands |
| `/ac enable 0/1/toggle` | Enable or disable the addon |
| `/ac slot 13/14` | Set which trinket slot to use |
| `/ac goggles 0/1` | Toggle engineering goggles swap |
| `/ac pvp 0/1` | Toggle riding gear in battlegrounds |
| `/ac swimming 0/1` | Toggle Azure Silk Belt while swimming |
| `/ac legacy 0/1` | Toggle legacy mode (Classic vs TBC gear) |
| `/ac button 0/1/reset/scale` | Toggle or configure the minimap button |
| `/ac reset` | Reset all settings (requires `/reload`) |

## Credits

Original addon by **Chromie** (Nethergarde Keep) - [CurseForge page](https://www.curseforge.com/wow/addons/autocrop)
