---
title: "Additional Quest Reward Types"
description: "This hack adds additional quest reward types."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack adds additional quest reward types.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=AdditionalQuestRewardTypes
```

# Additional Quest Types
## cards
The `cards` quest type actually exists in the base game, but is partially broken. This hack fixes it to work properly.

With this quest type, you can add a `car` reward that unlocks upon collecting all collector cards in a level.

**Note**: By default, there is no indicator you unlocked a reward but mods can use the [[CustomText.md]] hack to tweak the text shown when collecting all cards to convey this.