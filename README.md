# Every Build Exist Messages Protocol
This repository contains documentation on the PlayerIO based Every Build Exists API.  

Game Version: 2.3.4 (More protocol incoming)

## Table of contents
- [Game Information](#game-information)
- [Room Types](#room-types)
- [Receive Messages](#receive-messages)
  - [access](#rm-access)
  - [add](#rm-add)
  - [addedToCrew](#rm-addedToCrew)
  - [allowSpectating](#rm-allowSpectating)
  - [aura](#rm-aura)
  - [autotext](#rm-autotext)
  - [b](#rm-b) - Blocks
  - [backgroundColor](#rm-backgroundColor)
  - [badgeChange](#rm-badgeChange)
  - [banned](#rm-banned)      
  - [bc](#rm-bc) - Trophy Block    
  - [bco](#rm-bco) - Colored Blocks
  - [bn](#rm-bn) - NPC Blocks
  - [br](#rm-br) - Rotation Blocks
  - [bs](#rm-bs) - Sound Blocks
  - [bpo](#rm-bpo) - Counter Blocks
  - [bt](#rm-bt) - Tri-Backgrounds blocks
  - [bzo](#rm-bzo) - Vision Zone Blocks
  - [c](#rm-c)
  - [campaignRewards](#rm-campaignRewards)
  - [canAddToCrews](#rm-canAddToCrews)
  - [clear](#rm-clear)
  - [command](#rm-comand)
  - [completedLevel](#rm-completedLevel)
  - [confirm](#rm-confirm)
  - [crewAddRequest](#rm-crewAddRequest)
  - [crewAddRequestFailed](#rm-crewAddRequestFailed)
  - [dontPanic](#rm-dontPanic)
  - [editRights](#rm-editRights)
  - [effect](#rm-effect)
  - [effectlimits](#rm-effectlimits)
  - [face](#rm-face)
  - [favorited](#rm-favorited)
  - [givemagicbrickpackage](#rm-givemagicbrickpackage)
  - [givemagicsmiley](#rm-givemagicsmiley)
  - [god](#rm-god)
  - [hide](#rm-hide)
  - [hideLobby](#rm-hideLobby)
  - [hotbarSmileys](#rm-hotbarsmileys)
  - [image](#rm-images)
  - [info](#rm-info)
  - [info2](#rm-info2)
  - [init](#rm-init)
  - [init2](#rm-init2)
  - [joinCampaign](#rm-joinCampaign)
  - [k](#rm-k)
  - [kill](#rm-kill)
  - [ks](#rm-ks)
  - [lb](#rm-lb) - Label Blocks
  - [left](#rm-left)
  - [liked](#rm-liked)
  - [lobbyPreviewEnabled](#rm-lobbyPreviewEnabled)
  - [lockCampaign](#rm-lockCampaign)
  - [lostaccess](#rm-lostaccess)
  - [m](#rm-m)
  - [magic](#rm-magic)
  - [minimapEnabled](#rm-minimapEnabled)
  - [mod](#rm-mod)
  - [muted](#rm-muted)
  - [pm](#rm-pm)
  - [pointers](#rm-points)
  - [ps](#rm-ps)
  - [psi](#rm-psi)
  - [pt](#rm-pt) - Portal Blocks
  - [registercommand](#rm-registercommand)
  - [reset](#rm-reset)
  - [resetCoins](#rm-resetCoins)
  - [resetGlobalSwitches](#rm-resetGlobalSwitches)
  - [restoreProgress](#rm-restoreProgress)
  - [roomDescription](#rm-roomDescription)
  - [roomVisible](#rm-roomVisible)
  - [saved](#rm-saved)
  - [say](#rm-say)
  - [say_old](#rm-say_old)
  - [show](#rm-show)
  - [smileyGoldBorder](#rm-smileyGoldBorder)
  - [stoprun](#rm-stoprun)
  - [team](#rm-team)
  - [tele](#rm-tele)
  - [teleport](#rm-teleport)
  - [time](#rm-time)
  - [toggleGod](#rm-toggleGod)
  - [ts](#rm-ts) - Sign Blocks
  - [unfavorited](#rm-unfavorited)
  - [unliked](#rm-unliked)
  - [unregistercommand](#rm-unregistercommand)
  - [updatemeta](#rm-updatemeta)
  - [upgrade](#rm-upgrade)
  - [worldReleased](#rm-worldReleased)
  - [wp](#rm-wp) - World Portal Blocks
  - [write](#rm-write)
- [Send Messages](#send-messages)
  - [access](#sm-access)
  - [ToCrew](#sm-addToCrew)
  - [admin](#sm-admin)
  - [aura](#sm-aura)
  - [autosay](#sm-autosay)
  - [b](#sm-b)
  - [c](#sm-c)
  - [confirm](#sm-confirm)
  - [crown](#sm-crown)
  - [caketouch](#sm-caketouch)
  - [checkpoint](#sm-checkpoint)
  - [changeBadge](#sm-changeBadge)
  - [clear](#sm-clear)
  - [death](#sm-death)
  - [diamondtouch](#sm-diamondtouch)
  - [effect](#sm-effect)
  - [favorite](#sm-favorite)
  - [god](#sm-god)
  - [godblocktouch](#sm-godblock)
  - [hologramtouch](#sm-hologramtouch)
  - [hotbarSmileys](#sm-hotbarsmileys)
  - [init](#sm-init)
  - [init2](#sm-init2)
  - [key](#sm-key)
  - [kill](#sm-kill)
  - [levelcomplete](#sm-levelcomplete)
  - [like](#sm-like)
  - [m](#sm-m)
  - [mod](#sm-mod)
  - [name](#sm-name)
  - [pressKey](#sm-pressKey)
  - [pm](#sm-pm)
  - [ps](#sm-ps)
  - [registercommand](#sm-registercommand)
  - [rejectAddToCrew](#sm-rejectAddToCrew)
  - [requestAddToCrew](#sm-requestAddToCrew)
  - [reset](#sm-reset)
  - [resetCoins](#sm-resetCoins)
  - [save](#sm-save)
  - [say](#sm-say)
  - [setAllowSpectating](#sm-setAllowSpectating)
  - [setCurseLimit](#sm-setCurseLimit)
  - [setHideLobby](#sm-setHideLobby)
  - [setLobbyPreviewEnabled](#sm-setLobbyPreviewEnabled)
  - [setMinimapEnabled](#sm-setMinimapEnabled)
  - [setRoomDescription](#sm-setRoomDescription)
  - [setRoomVisible](#sm-setRoomVisible)
  - [setStatus](#sm-setStatus)
  - [setZombieLimit](#sm-setZombieLimit)
  - [smiley](#sm-smiley)
  - [smileyGoldBorder](#sm-smileyGoldBorder)
  - [system](#sm-botwrite)
  - [team](#sm-team)
  - [time](#sm-time)
  - [touch](#sm-touch)
  - [unfavorite](#sm-unfavorite)
  - [unlike](#sm-unlike)
  - [unregistercommand](#sm-unregistercommand)
- [Models](#models)
  - [Auto Text](#model-auto-text)
  - [Badges](#model-badges)
  - [Campaign Status](#model-campaign-status)
  - [Colored Blocks](#model-cblocks)
  - [Crew World Status](#model-crew-status)
  - [Effects](#model-effects)
  - [Keys](#model-keys)
  - [Teams](#model-teams)

___

# <a id="game-information">Game Information</a>
```
GameID = every-build-exists-d6aoqro023pzodrp9jhw
Version = 233
```

*NOTE: the game ID is required to log into PlayerIO to send requests.*

# <a id="room-types">Room Types</a>

| Type        | Room Name | Description
| ----        | --------- |  --------- 
| Normal      | Everybuildexists{version} | Join the EBE Worlds. To use/read commands, read inside this document. |
| Public | Public | Join the EBE Worlds. To use/read commands, read inside this document.
| Beta        | Beta{version} | Join Beta worlds. To use/read commands, read inside this document. |
| Lobby       | Lobby{version} | Join Lobby. If you want to execute commands or read them, look in [Lobby documentations](https://github.com/capashaa/EBEProtocol/blob/main/Lobby.md). |
| Crew Lobby  | CrewLobby{version} | Join crew lobby |
| Lobby Guest | LobbyGuest{version} | Join Guest lobby |

(Replace {version} with the current version)  
Or use:
 ``client.BigDB.Load("config","config")["version"]``
To be able to getting latest version.

# <a id="receive-messages">Receive messages</a>

### <a id="rm-access">"access"</a>
Occurs when you are given edit rights in the world.

*(This event does not contain any other information.)*

### <a id="rm-add">"add"</a>
Occurs when someone joins the world.

| Id   | Type        | Name               | Description
| ---  | ---         | ----               | -----------
| `0`  | `Integer`   | Id                 | The player's id.
| `1`  | `String`    | Username           | The player's username.
| `2`  | `String`    | ConnectUserId      | The player's unique user id.
| `3`  | `Integer`   | Shape              | The player's smiley shape.
| `4`  | `Integer`   | Colour             | The player's smiley colour.
| `5`  | `Integer`   | Border             | The player's smiley border.
| `6`  | `Integer`   | Eyes               | The player's smiley eyes.
| `7`  | `Integer`   | Mouth              | The player's smiley mouth.
| `8`  | `Integer`   | Addon              | The player's smiley addon.
| `9`  | `Integer`   | Above              | The player's smiley above.
| `10`  | `Integer`   | Below              | The player's smiley below.
| `11`  | `Integer`   | Wings              | The player's smiley wings.
| `12`  | `Double`    | X                  | The x coordinate of the player's position.
| `13`  | `Double`    | Y                  | The y coordinate of the player's position.
| `14`  | `Boolean`   | God Mode           | Value indicating whether the player is in god mode.
| `15`  | `Boolean`   | Moderator Mode         | Value indicating whether the player is in moderator mode.
| `16`  | `Boolean`   | Can Chat           | Value indicating whether the player is allowed to chat.
| `17`  | `Integer`   | Gold Coins         | The amount of player's gold coins.
| `18` | `Integer`   | Blue Coins         | The amount of player's blue coins.
| `19` | `Integer`   | Deaths             | The amount of player's deaths.
| `20` | `Boolean`   | Is Friend          | Value indicating whether the player is a friend.
| `21` | `Boolean`   | Gold Membership    | Value indicating whether the player has gold membership.
| `22` | `Integer`   | Team               | The player's team id.  *See [Teams](#model-teams).*
| `23` | `Integer`   | Aura Shape         | The player's aura shape id. *See [Auras](#model-aura)*
| `24` | `Integer`   | Aura Color         | The player's aura color id. *See [Aura Colors](#model-aura-color)*
| `25` | `Uint`      | Chat Color         | The player's chat color.
| `26` | `String`    | Badge              | The player's badge id. *See [Badges](#model-badges).*
| `27` | `Boolean`   | Crew Member        | Value indicating whether the player is a member of the crew to which belongs this world.
| `28` | `ByteArray` | Purple Switches    | Byte array of purple switch states.
| `29` | `Boolean`   | Can Edit           | Value indicating whether the player can edit in this world.
| `30` | `Boolean`   | Can Toggle Godmode | Value indicating whether the player can toggle godmode or not.  
| `31` | `Integer` | Total Pointers | How many pointers the player have.  
|`[...]` | `Uint` | Pointer color | The pointer color 
|`[...]` | `int` | Pointer value | The pointer value  
> **NOTE:** This can only be received by the world owner.

### <a id="rm-addedToCrew">"addedToCrew"</a>
Occurs when a world was successfully added to a crew.

| Id  | Type     | Name      | Description
| --- | ----     | ----      | -----------
| `0` | `String` | Crew Id   | The id of the crew to which the world was added.
| `1` | `String` | Crew Name | The name of the crew to which the world was added.

### <a id="rm-allowSpectating">"allowSpectating"</a>
Occurs when the spectating is allowed setting is changed.

| Id  | Type      | Name    | Description
| --- | ----      | ----    | -----------
| `0` | `Boolean` | Allowed | Value indicating whether spectating is allowed.

### <a id="rm-aura">"aura"</a>
Occurs when a player changed their aura shape and/or color.

| Id  | Type      | Name       | Description
| --- | ----      | ----       | -----------
| `0` | `Integer` | Player Id  | The player's id.
| `1` | `Integer` | Aura Shape | The aura shape id. *See [Auras](#model-aura)*
| `2` | `Integer` | Aura Color | The aura color id. *See [Aura Colors](#model-aura-color)*

### <a id="rm-autotext">"autotext"</a>
Occurs when a player uses auto-text.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.
| `1` | `String`  | Auto-Text | The automatic text value. *See [Auto Text](#model-auto-text).*

### <a id="rm-b">"b"</a>
Occurs when a block is placed in the world.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Layer     | The layer id.
| `1` | `UInt`    | X         | The x coordinate of the block's position.
| `2` | `UInt`    | Y         | The y coordinate of the block's position.
| `3` | `UInt`    | Block Id  | The block id.
| `4` | `UInt`    | Player Id | The id of the player which placed this block.

### <a id="rm-backgroundColor">"backgroundColor"</a>
Occurs when the background color of the world is changed.

| Id  | Type   | Name  | Description
| --- | ----   | ----  | -----------
| `0` | `UInt` | Color | The color of the background. **NOTE:** transparent color means the custom background color is disabled.

### <a id="rm-badgeChange">"badgeChange"</a>
Occurs when a player changes their badge.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.
| `1` | `String`  | Badge     | The badge id. *See [Badges](#model-badges).*

### <a id="rm-banned">"banned"</a>
Occurs when trying to join a world with a banned account.

### <a id="rm-bc">"bc"</a>
Occurs when a block with a number value is placed in the world or effect.

| Id  | Type   | Name         | Description
| --- | ----   | ----         | -----------
| `0` | `UInt` | X            | The x coordinate of the block's position.
| `1` | `UInt` | Y            | The y coordinate of the block's position.
| `2` | `UInt` | Block Id     | The block's id.
| `3` | `UInt` | Number Value | The number value.
| `4` | `UInt` | Player Id    | The id of the player which placed this block.

### <a id="rm-bco">"bco"</a>
Occurs when a block that is using a hex color.  
Backgrounds, Foregrounds, Spikes.  

| Id  | Type   | Name         | Description
| --- | ----   | ----         | -----------
| `0` | `UInt` | X            | The x coordinate of the block's position.
| `1` | `UInt` | Y            | The y coordinate of the block's position.
| `2` | `UInt` | Block Id     | The block's id.
| `3` | `UInt` | Colour       | The decimal number of the colour.
| `4` | `Integer`  | Layer    | The layer of the block.
| `5` | `Integer` | Rotation  | The rotation of the block. (if -1, no rotation)
| `6` | `UInt` | Player Id    | The id of the player which placed this block.



### <a id="rm-bn">"bn"</a>
Occurs when placing a NPC in the world.

| Id  | Type     | Name         | Description
| --- | ----     | ----         | -----------
| `0` | `UInt`   | X            | The x coordinate of the NPC position.
| `1` | `UInt`   | Y            | The y coordinate of the NPC position.
| `2` | `UInt`   | NPC Block Id | The NPC Block Id. See [NPC's ids](#model-npcid).
| `3` | `String` | NPC Name     | The name of the NPC.
| `4` | `String` | NPC Text     | The first text from the NPC
| `5` | `String` | NPC Text     | The second text from the NPC
| `6` | `String` | NPC Text     | The third text from the NPC
| `7` | `UInt`   | Player Id    | The id of the player which placed this NPC.


### <a id="rm-br">"bpo"</a>
Occurs when a counter block is placed.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `UInt`    | X         | The x coordinate of the block's position.
| `1` | `UInt`    | Y         | The y coordinate of the block's position.
| `2` | `UInt`    | Block Id  | The block's id.
| `3` | `Integer`    | Amount    | The amount.
| `4` | `Uint` | Colour     | The colour of the block.
| `5` | `UInt`    | Player Id | The id of the player which placed this block.



### <a id="rm-br">"br"</a>
Occurs when a morphable block is placed in the world or Gravity Effect.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `UInt`    | X         | The x coordinate of the block's position.
| `1` | `UInt`    | Y         | The y coordinate of the block's position.
| `2` | `UInt`    | Block Id  | The block's id.
| `3` | `UInt`    | Morph     | The morph id.
| `4` | `Integer` | Layer     | The layer id.
| `5` | `UInt`    | Player Id | The id of the player which placed this block.

### <a id="rm-bs">"bs"</a>
Occurs when a sound block is placed in the world.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `UInt`    | X         | The x coordinate of the block's position.
| `1` | `UInt`    | Y         | The y coordinate of the block's position.
| `2` | `UInt`    | Block Id  | The block id.
| `3` | `Integer` | Sound Id  | The sound id.
| `4` | `UInt`    | Player Id | The id of the player which placed this block.

### <a id="rm-bt">"bt"</a>
Occurs when a tribackground is placed.

| Id  | Type      | Name         | Description
| --- | ----      | ----         | -----------
| `0` | `UInt`    | X            | The x coordinate of the block's position.
| `1` | `UInt`    | Y            | The y coordinate of the block's position.
| `2` | `UInt`    | Block Id     | The block id.
| `3` | `Uint`    | Rotation Id  | The rotation value.
| `4` | `Integer` | Colour       | The colour of the block.  
| `3` | `Uint`    | Player Id    | The id of the player which placed this block.

### <a id="rm-bzo">"bzo"</a>
Occurs when a vision block is placed.

| Id  | Type      | Name         | Description
| --- | ----      | ----         | -----------
| `0` | `UInt`    | X            | The x coordinate of the block's position.
| `1` | `UInt`    | Y            | The y coordinate of the block's position.
| `2` | `UInt`    | Block Id     | The block id.
| `3` | `Uint`    | Rotation Id  | The rotation value.
| `4` | `Uint`    | Player Id    | The id of the player which placed this block.

### <a id="rm-c">"c"</a>
Occurs when a player gets a blue or gold coin.

| Id  | Type      | Name       | Description
| --- | ----      | ----       | -----------
| `0` | `Integer` | Player Id  | The player's id.
| `1` | `Integer` | Gold Coins | The amount of collected gold coins.
| `2` | `Integer` | Blue Coins | The amount of collected blue coins.
| `3` | `UInt`    | X          | The x coordinate of the coin's position.
| `4` | `UInt`    | Y          | The y coordinate of the coin's position.

### <a id="rm-campaignRewards">"campaignRewards"</a>
Occurs when recieving a reward for completing a campaign world.

| Id  | Type      | Name           | Description
| --- | ----      | ----           | -----------
| `0` | `Boolean` | Received Badge | Value indicating whether received a badge.

This message has 2 possible outcomes:

-- If the player received a badge:

| Id  | Type     | Name              | Description
| --- | ----     | ----              | -----------
| `1` | `String` | Badge Title       | The title of the badge.
| `2` | `String` | Badge Description | The description of the badge.
| `3` | `String` | Badge URL         | The image URL of the badge.

-- If the player didn't receive a badge:

| Id  | Type     | Name      | Description
| --- | ----     | ----      | -----------
| `1` | `String` | World URL | The image URL of the next world in the campaign.

Both outcomes are followed with list of rewards:

| Id      | Type     | Name     | Description
| ---     | ----     | ----     | -----------
| `[...]` | `String` | Id       | The id of the reward.
| `[...]` | `UInt`   | Quantity | The quantity of the reward.

### <a id="rm-canAddToCrews">"canAddToCrews"</a>
Occurs after initialization. Contains information about crews to which current world can be added.

| Id      | Type     | Name      | Description
| ---     | ----     | ----      | -----------
| `[...]` | `String` | Crew Id   | The id of the crew.
| `[...]` | `String` | Crew Name | The name of the crew.

Repeated for each valid crew.

### <a id="rm-clear">"clear"</a>
Occurs when the world is cleared.

| Id  | Type      | Name            | Description
| --- | ----      | ----            | -----------
| `0` | `Integer` | Width           | The width of the world.
| `1` | `Integer` | Height          | The height of the world.
| `2` | `UInt`    | Border color | The color of the block used as a world border.
| `3` | `UInt`    | Fill Block Id   | The id of the block used to fill the world.

### <a id="rm-command">"command"</a>
Received by bot account once a user uses a custom slash command.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `Integer` | Player ID | The Player's id that used the command.  
| `1` | `String`  | cmdName | Command Name.
| `[...]` | `String`  | Arguments | The arguments from user.

### <a id="rm-completedLevel">"completedLevel"</a>
Occurs when touching a win trophy (completing the world.)

**NOTE:** If player received campaign rewards, the ["campaignRewards"](#rm-campaignRewards) message is received instead.

### <a id="rm-confirm">"confirm"</a>
Received by staff if the world is set to friends only or nobody.   
It will ask if you want to join or not.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `String` | Message | Confirm message.  
| `1` | `String`  | Message | Why you can't join the world.

### <a id="rm-crewAddRequest">"crewAddRequest"</a>
Occurs when a player requests to add the world to their crew.

| Id  | Type     | Name      | Description
| --- | ----     | ----      | -----------
| `0` | `String` | Username  | The username of the player which requested the add the world to their crew.
| `1` | `String` | Crew Name | The name of the crew to which they want to add the world.

**NOTE:** If this fails, the ["crewAddRequestFailed"](#rm-crewAddRequestFailed) message is received instead.

### <a id="rm-crewAddRequestFailed">"crewAddRequestFailed"</a>
Occurs when an attempt to request adding of the world to a crew didn't succeed.
(For example when the world owner wasn't online in the world or rejected the request.)

| Id  | Type     | Name   | Description
| --- | ----     | ----   | -----------
| `0` | `String` | Reason | The reason of the failure.

### <a id="rm-dontPanic">"dontPanic"</a>
Plays a sound clip from "The Hitchhiker's Guide to the Galaxy", logs "* SYSTEM: Don't panic.", and gives the user the Computer NPC.
Occurs when the player has exactly 42 gold coins, 42 blue coins, and 42 deaths.

### <a id="rm-editRights">"editRights"</a>
Occurs when a player receives or loses edit rights.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.
| `1` | `Boolean` | Can Edit  | Value indicating whether the player is now allowed to edit in the world.

**NOTE:** You can only receive this message if you are the world owner.

### <a id="rm-effect">"effect"</a>
Occurs when a player gains or loses an effect.

| Id  | Type      | Name      | Required? | Description
| --- | ----      | ----      | --------- | -----------
| `0` | `Integer` | Player Id | Required  | The player's id.
| `1` | `Integer` | Effect    | Required  | The effect's id. *See [Effects](#model-effects).*
| `2` | `Boolean` | Enabled   | Required  | Value indicating whether the effect is enabled.
| `3` | `Double`  | Argument  | Optional  | The optional argument of the effect (time left, number of jumps, etc.)
| `4` | `Integer` | Duration  | Optional  | The duration of the effect.

### <a id="rm-effectlimits">"effectlimits"</a>
Occurs when effect limits are changed.

| Id  | Type      | Name         | Description
| --- | ----      | ----         | -----------
| `0` | `Integer` | Curse Limit  | The curse limit.
| `1` | `Integer` | Zombie Limit | The zombie limit.

### <a id="rm-face">"face"</a>
Occurs when someone changes their smiley.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.
| `1` | `Integer` | Shape | The player's smiley shape.
| `2` | `Integer` | Colour | The player's smiley colour.
| `3` | `Integer` | Border | The player's smiley border.
| `4` | `Integer` | Eyes | The player's smiley eyes.
| `5` | `Integer` | Mouth | The player's smiley mouth.
| `6` | `Integer` | Addon | The player's smiley addon.
| `7` | `Integer` | Above | The player's smiley above.
| `8` | `Integer` | Below | The player's smiley below.
| `9` | `Integer` | Wings  | The player's smiley wings.  

Use this code as example to be able to read different faces:  
[https://pastebin.com/kdZg5rAv](https://pastebin.com/kdZg5rAv) 

### <a id="rm-favorited">"favorited"</a>
Occurs when you favorited the world.

### <a id="rm-givemagicbrickpackage">"givemagicbrickpackage"</a>
Occurs when you are given a magic brick package.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `String` | Package | The id of the magic brick package.

### <a id="rm-givemagicsmiley">"givemagicsmiley"</a>
Occurs when you are given a magic smiley.

| Id  | Type     | Name   | Description
| --- | ----     | ----   | -----------
| `0` | `String` | Smiley | The id of the magic smiley.

### <a id="rm-god">"god"</a>
Occurs when a player toggles god mode.

| Id  | Type      | Name           | Description
| --- | ----      | ----           | -----------
| `0` | `Integer` | Player Id      | The player's id.
| `1` | `Boolean` | Is In God Mode | Value indicating whether this player is now in god mode.

### <a id="rm-hide">"hide"</a>
Occurs when a player touches a key or when timed doors change their state.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `String`  | Key       | The name of the key (or timed door). *See [Keys](#model-keys).*
| `1` | `Integer` | Player Id | The player's id.|

### <a id="rm-hideLobby">"hideLobby"</a>
Occurs when "world hidden in the lobby setting" is changed.

| Id  | Type      | Name   | Description
| --- | ----      | ----   | -----------
| `0` | `Boolean` | Hidden | Value indicating whether the world is hidden from the lobby and profile.

### <a id="rm-hotbarsmileys">"hotbarSmileys"</a>
Your 10 favorite smileys. Occurs when joining a world.

| Id  | Type      
| --- | ----      
| `0-10` | `Integer`

### <a id="rm-images">"info"</a>
Occurs when the world contains images or been added.

| Id  | Type      | Name           | Description
| --- | ----      | ----           | -----------
| `0` | `String`  | Name           | The name of the image.
| `1` | `Integer` | Position X     | The X position where the image should be drawn at.
| `2` | `Integer` | Position Y     | The Y position where the image should be drawn at.

### <a id="rm-info">"info"</a>
Occurs when the server sends information saying that:
- you were kicked
- the room is full
- and/or, the rate limit was exceeded

| Id  | Type     | Name           | Description
| --- | ----     | ----           | -----------
| `0` | `String` | Title          | The Title of the message.
| `1` | `String` | Text           | The Text of the message.
| `2` | `Boolean`| Modal          | ?.
| `3` | `String` | Image          | The Image for the message. Or null.
| `4` | `String` | Sound          | The Sound for the message. Or null.


### <a id="rm-info2">"info2"</a>
Occurs when the server sends low priority information that can be displayed in an non-invasive pop-up.

| Id  | Type     | Name   | Description
| --- | ----     | ----   | -----------
| `0` | `String` | Title  | The title for the message.
| `1` | `String` | Text   | The text for the message.
| `2` | `String` | Sound  | The sound for the message. Or null.

### <a id="rm-init">"init"</a>
Occurs when the player initially joins the room.

| Id      | Type        | Name                       | Description
| ---     | ----        | ----                       | -----------
| `0`     | `String`    | Owner Username             | The username of the world owner.
| `1`     | `String`    | World Name                 | The world name.
| `2`     | `Integer`   | Plays                      | The amount of plays.
| `3`     | `Integer`   | Favorites                  | The amount of favorites.
| `4`     | `Integer`   | Likes                      | The amount of likes.
| `5`     | `Integer`   | Player Id                  | The player's id.
| `6`     | `Integer`   | SmileyShape                | The player's smiley shape.
| `7`     | `Integer`   | SmileyColour               | The player's smiley colour.
| `8`     | `Integer`   | SmileyBorder               | The player's smiley border.
| `9`     | `Integer`   | SmileyEyes               | The player's smiley eyes.
| `10`     | `Integer`   | SmileyMouth               | The player's smiley mouth.
| `11`     | `Integer`   | SmileyAddon               | The player's smiley addon.
| `12`     | `Integer`   | SmileyAbove                | The player's smiley above.
| `13`     | `Integer`   | SmileyBelow               | The player's smiley below.
| `14`     | `Integer`   | SmileyWings                | The player's smiley wings.
| `15`     | `Integer`   | Aura Shape                 | The player's aura shape id. *See [Auras](#model-aura)*
| `16`     | `Integer`   | Aura Color                 | The player's aura color id. *See [Aura Color](#model-aura-color)*
| `17`    | `Double`    | X                          | The x coordinate of the player's spawn position.
| `18`    | `Double`    | Y                          | The y coordinate of the player's spawn position.
| `19`    | `UInt`      | Chat Color                 | The player's chat color.
| `20`    | `String`    | Username                   | The player's username.
| `21`    | `Boolean`   | Can Edit                   | Value indicating whether the player can edit.
| `22`    | `Boolean`   | Is Owner                   | Value indicating whether the player is world owner.
| `23`    | `Boolean`   | Favorited                  | Value indicating whether the player has favorited this world.
| `24`    | `Boolean`   | Liked                      | Value indicating whether the player has liked this world.
| `25`    | `Integer`   | World Width                | The width of the world.
| `26`    | `Integer`   | World Height               | The height of the world.
| `27`    | `Double`    | World Gravity Multiplier   | The world's gravity multiplier.
| `28`    | `UInt`      | Background Color           | The color of the background. **NOTE:** Transparent color means that the custom background color is disabled.
| `29`    | `Boolean`   | Accessible                 | Value indicating whether this world is accessible by other players.
| `30`    | `Boolean`   | Hidden From Lobby          | Value indicating whether this world is hidden from the lobby and profile.
| `31`    | `Boolean`   | Spectating Allowed         | Value indicating whether spectating in this world is allowed.
| `32`    | `String`    | Description                | The description of the world.
| `33`    | `Integer`   | Curse Limit                | The curse limit.
| `34`    | `Integer`   | Zombie Limit               | The zombie limit.
| `35`    | `Boolean`   | Belongs To Campaign        | Value indicating whether this world is part of a campaign.
| `36`    | `String`    | Crew Id                    | The id of the crew to which belongs this world.
| `37`    | `String`    | Crew Name                  | The name of the crew to which belongs this world.
| `38`    | `Boolean`   | Can Change World Options   | Value indicating whether the player can change world options.
| `39`    | `Integer`   | Crew Status                | The crew status of the world. *See [Crew World Status](#model-crew-status).*
| `40`    | `String`    | Badge                      | The player's badge id. *See [Badges](#model-badges).*
| `41`    | `Boolean`   | Is Crew Member             | Value indicating whether the player is a member of the crew to which belongs this world.
| `42`    | `Boolean`   | Minimap Enabled            | Value indicating whether the minimap is enabled in this world.
| `43`    | `Boolean`   | Lobby Preview Enabled      | Value indicating whether the lobby preview is enabled in this world.
| `44`    | `ByteArray` | Orange Switches            | Byte array with states of orange switches
| `45`    | `Boolean`   | FriendsOnly                | If the world is set to friends only
| `46`    | `String`    | OwnerId                    | The owners ID.
| `47`    | `Boolean`   | Can toggle godmode         | If the user can toggle godmode.
| `48`    | `String`    | ws                         | Indicates the start of the world data.
| `49` | `ByteArray`     | The serialized world data. | Indicates the world data.
| `50` | `String`    | we                         | Indicates the end of the world data.

**How to read the ByteArray:**  
You need: [BitConverter](https://pastebin.com/TNJe3ZEb)  
How to Read: [Example Code](https://pastebin.com/K6UQFqUN)

### <a id="rm-init2">"init2"</a>
Occurs when joining world is completed.

### <a id="rm-joinCampaign">"joinCampaign"</a>
Occurs when a player joins a campaign world.

| Id  | Type      | Name   | Description
| --- | ----      | ----   | -----------
| `0` | `String`  | Title  | The title of the campaign.
| `1` | `Integer` | Status | The campaign status. *See [Campaign Status](#model-campaign-status).*

Additional parameters received when the campaign world is unlocked:

| Id  | Type      | Name       | Description
| --- | ----      | ----       | -----------
| `2` | `Integer` | Difficulty | The campaign difficulty.
| `3` | `Integer` | Tier       | The campaign tier of this world.
| `4` | `Integer` | Tiers      | The amount of tiers in the campaign.

### <a id="rm-k">"k"</a>
Occurs when a player touches a gold crown.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id. **NOTE:** Set to `-1` if there is no player with a crown.

### <a id="rm-kill">"kill"</a>
Occurs when a player is killed due to an expired effect or /kill, /killall commands.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.

### <a id="rm-ks">"ks"</a>
Occurs when a player touches a silver crown.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.

### <a id="rm-lb">"lb"</a>
Occurs when a player places a label block.
> ID: 1000

| Id  | Type      | Name       | Description
| --- | ----      | ----       | -----------
| `0` | `UInt`    | X          | The x coordinate of the block's position.
| `1` | `UInt`    | Y          | The y coordinate of the block's position.
| `2` | `Integer` | Block Id   | The id of the block.
| `3` | `String`  | Text       | The text.
| `4` | `String`  | Text Color | The color of the text.
| `5` | `UInt`    | Player Id  | The id of the player which placed this block.

### <a id="rm-left">"left"</a>
Occurs when a player leaves the world.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.

### <a id="rm-liked">"liked"</a>
Occurs when you liked the world.

### <a id="rm-lobbyPreviewEnabled">"lobbyPreviewEnabled"</a>
Occurs when the lobby preview is enabled or disabled.

| Id  | Type      | Name    | Description
| --- | ----      | ----    | -----------
| `0` | `Boolean` | Enabled | Value indicating whether the lobby preview is now enabled.

### <a id="rm-lockCampaign">"lockCampaign"</a>
Occurs when you are locked out of campaign.
This means that you can no longer complete it or receive rewards without rejoining the world.

| Id  | Type     | Name          | Description
| --- | ----     | ----          | -----------
| `0` | `String` | Campaign Name | The name of the campaign.

### <a id="rm-lostaccess">"lostaccess"</a>
Occurs when you lose edit rights.

### <a id="rm-m">"m"</a>
Occurs when a player moves.

| Id  | Type      | Name                 | Description
| --- | ----      | ----                 | -----------
| `0` | `Integer` | Player Id            | The player's id.
| `1` | `Double`  | X                    | The x coordinate of the player's position.
| `2` | `Double`  | Y                    | The y coordinate of the player's position.
| `3` | `Double`  | Horizontal Speed     | The horizontal speed.
| `4` | `Double`  | Vertical Speed       | The vertical speed.
| `5` | `Double`  | Horizontal Modifier  | The horizontal movement modifier.
| `6` | `Double`  | Vertical Modifier    | The vertical movement modifier.
| `7` | `Integer` | Horizontal Direction | The horizontal movement direction indicator. *(`-1` means left, `1` means right and `0` means that player is not moving horizontally.)*
| `8` | `Integer` | Vertical Direction   | The vertical movement direction indicator. *(`-1` means up, `1` means down and `0` means that player is not moving vertically.)*
| `9` | `Boolean` | Space Pressed        | Value indicating whether the player is holding down space-bar.
| `10`| `Boolean` | Space Just Pressed   | Value indicating whether the player has just pressed down space-bar.

### <a id="rm-magic">"magic"</a>
Occurs when you are given a magic reward.  
Will also play a sound.

### <a id="rm-minimapEnabled">"minimapEnabled"</a>
Occurs when the minimap's visibility is changed.

| Id  | Type      | Name            | Description
| --- | ----      | ----            | -----------
| `0` | `Boolean` | Minimap Enabled | Value indicating whether the minimap is enabled or not.

### <a id="rm-mod">"mod"</a>
Occurs when player goes into Moderator Mode.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.  
| `1` | `Boolean` | Moderator Mode     | Value indicating whether the player is in moderator mode or not.  

### <a id="rm-muted">"muted"</a>
Occurs when you muted or un-muted a player.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.
| `1` | `Boolean` | Muted     | Value indicating whether the player is muted.

### <a id="rm-pm">"pm"</a>
Occurs when a player send a private message

| Id  | Type      | Name        | Description
| --- | ----      | ----        | -----------
| `0` | `Integer` | Player Id   | The player's id.
| `1` | `String`  | Message     | The message from you or sent to you
| `2` | `Boolean` | Incoming    | Incoming means the message is sent to you (true), or from you (false)

### <a id="rm-points">"points"</a>  
Occurs when a player touches pointers  
| Id  | Type      | Name        | Description
| --- | ----      | ----        | -----------
| `0` | `Integer` | Player Id   | The player's id.
| `1` | `Integer`  | Value     | The pointer value.
| `2` | `Uint` | Color        | The color of the pointer.
| `3` | `Boolean` | Reusable      | Reusable or not.

### <a id="rm-ps">"ps"</a>
Occurs when a player touches a switch.

| Id  | Type      | Name        | Description
| --- | ----      | ----        | -----------
| `0` | `Integer` | Player Id   | The player's id.
| `1` | `UInt`    | Switch Type | The type of the switch. Purple = 0 and 1 = orange.
| `2` | `Integer` | Switch Id   | The switch id.
| `3` | `Boolean` | Enabled     | Value indicating whether the switch is enabled.

### <a id="rm-psi">"psi"</a>
Occurs when initial switch states are sent after you join the world.

| Id  | Type        | Name          | Description
| --- | ----        | ----          | -----------
| `0` | `Integer`   | Player Id     | The player's id.
| `1` | `ByteArray` | Switch States | The byte array describing initial switch states.

### <a id="rm-pt">"pt"</a>
Occurs when a portal is placed in the world.
| Id  | Type      | Name            | Description
| --- | ----      | ----            | -----------
| `0` | `UInt`    | X               | The x coordinate of the block's position.
| `1` | `UInt`    | Y               | The y coordinate of the block's position.
| `2` | `UInt`    | Block Id        | The block id.
| `3` | `UInt`    | Portal Rotation | The portal rotation.
| `4` | `UInt`    | Portal Id       | The portal id.
| `5` | `UInt`    | Portal Target   | The portal target id.
| `6` | `Integer` | Player Id       | The id of the player which placed this block.



### <a id="rm-registercommand">"registercommand"</a>
Received once a command is registered.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `Boolean` | Success | If the command is successfully added.
| `1` | `String`  | cmdName/ErrorMsg | Command Name or Error message.




### <a id="rm-reset">"reset"</a>
Occurs when world is reverted to the last save using the /loadlevel command.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `String` | ws      | Indicates the start of the world data.
| `1` | `ByteArray`  | Data | The serialized world data.
| `n` | `String` | we      | Indicates the end of the world data.

### <a id="rm-resetCoins">"resetCoins"</a>  
Occurs when player is touching resetCoins block.
| Id  | Type     | Name    | Description  
| --- | ----     | ----    | -----------  
| `0` | `Integer` | Player Id      | The player's id.  
| `1` | `Boolean`  | Coin type | True = orange, False = blue.  

### <a id="rm-resetGlobalSwitches">"resetGlobalSwitches"</a>
Occurs when global switches are reset.

### <a id="rm-restoreProgress">"restoreProgress"</a>
Occurs when your campaign progress is restored.

| Id   | Type        | Name             | Description
| ---  | ----        | ----             | -----------
| `0`  | `Integer`   | Player Id        | The player's id.
| `1`  | `Double`    | X                | The x coordinate of the player's position.
| `2`  | `Double`    | Y                | The y coordinate of the player's position.
| `3`  | `Integer`   | Gold Coins       | The amount of collected gold coins.
| `4`  | `Integer`   | Blue Coins       | The amount of collected blue coins.
| `5`  | `ByteArray` | Gold Coin X      | The x coordinates array of the gold coins positions.
| `6`  | `ByteArray` | Gold Coin Y      | The y coordinates array of the gold coins positions.
| `7`  | `ByteArray` | Blue Coin X      | The x coordinates array of the blue coins positions.
| `8`  | `ByteArray` | Blue Coin Y      | The y coordinates array of the blue coins positions.
| `9`  | `Integer`   | Deaths           | The amount of deaths.
| `10` | `UInt`      | Spawn X          | The x coordinate of the player's checkpoint position.
| `11` | `UInt`      | Spawn Y          | The y coordinate of the player's checkpoint position.
| `12` | `ByteArray` | Switch States    | The byte array describing purple switches states.
| `13` | `Double`    | Horizontal Speed | The horizontal movement speed.
| `14` | `Double`    | Vertical Speed   | The vertical movement speed.
| `15` | `Boolean`   | IsinGodmode      | If the player is in godmode.

### <a id="rm-roomDescription">"roomDescription"</a>
Occurs when the world description is changed.

| Id  | Type     | Name        | Description
| --- | ----     | ----        | -----------
| `0` | `String` | Description | The world description.

### <a id="rm-roomVisible">"roomVisible"</a>
Occurs when the world accessibility is changed.

| Id  | Type      | Name       | Description
| --- | ----      | ----       | -----------
| `0` | `Boolean` | Accessible | Value indicating whether the world is now accessible by other players.
| `1` | `Boolean` | Friends    | Value indicating whether the world is now accessible by friends only.

### <a id="rm-saved">"saved"</a>
Occurs when you saved the world.

### <a id="rm-say">"say"</a>
Occurs when a player sends a chat message.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.
| `1` | `String`  | Text      | The chat message text.

### <a id="rm-say_old">"say_old"</a>
Occurs after you join a world and a snippet of the chat is played back.

| Id  | Type      | Name       | Description
| --- | ----      | ----       | -----------
| `0` | `String`  | Username   | The sender's username.
| `1` | `String`  | Text       | The text of the chat message.
| `2` | `Boolean` | Is Friend  | Value indicating whether the player is a friend.
| `3` | `UInt`    | Chat Color | The chat color of the sender.

### <a id="rm-show">"show"</a>
Occurs when a key deactivates or timed doors change their state.

| Id  | Type     | Name | Description
| --- | ----     | ---- | -----------
| `0` | `String` | Key  | The name of the key (or timed door). *See [Keys](#model-keys).*

### <a id="rm-smileyGoldBorder">"smileyGoldBorder"</a>
Occurs when someone enables or disables the gold smiley border.

| Id  | Type      | Name               | Description
| --- | ----      | ----               | -----------
| `0` | `Integer` | Player Id          | The player's id.
| `1` | `Boolean` | Gold Smiley Border | Value indicating whether the player is wearing gold smiley border.

### <a id="rm-stoprun">"stoprun"</a>
Occurs when someone enter moderator mode or gets god mode. (/givegod player)

| Id  | Type      | Name               | Description
| --- | ----      | ----               | -----------
| `0` | `Boolean` | in Trialsmode      | If the world is in trialsmode.

### <a id="rm-team">"team"</a>
Occurs when a player changes their team.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.
| `1` | `Integer` | Team      | The team id. *See [Teams](#model-teams).*

### <a id="rm-tele">"tele"</a>
Occurs when one or more players are teleported or respawned (including death.)

| Id  | Type      | Name           | Description
| --- | ----      | ----           | -----------
| `0` | `Boolean` | Reset Players  | Value indicating whether the player's properties were reset.
| `1` | `Boolean` | Reset Switches | Value indicating whether orange switches were reset.

Repeated for each teleported player:

| Id      | Type      | Name      | Description
| ---     | ----      | ----      | -----------
| `[...]` | `Integer` | Player Id | The player's id.
| `[...]` | `Double`  | X         | The x coordinate of the player's respawn position.
| `[...]` | `Double`  | Y         | The y coordinate of the player's respawn position.
| `[...]` | `Integer` | Deaths    | The amount of player's deaths.

### <a id="rm-teleport">"teleport"</a>
Occurs when a player is teleported to another location.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The player's id.
| `1` | `Integer` | X         | The x coordinate of the player's position.
| `2` | `Integer` | Y         | The y coordinate of the player's position.

### <a id="rm-time">"time"</a>
Occurs as a response to the ["time"](#sm-time) send message.

| Id  | Type     | Name | Description
| --- | ----     | ---- | -----------
| `0` | `Double` | Data | The previously sent data.
| `1` | `Double` | Time | The current server time.

### <a id="rm-toggleGod">"toggleGod"</a>
Occurs when a player received or lost the ability to toggle god mode.

| Id  | Type      | Name           | Description
| --- | ----      | ----           | -----------
| `0` | `Integer` | Player Id      | The player's id.
| `1` | `Boolean` | Can Toggle God | Value indicating whether the player can now toggle god mode.

### <a id="rm-ts">"ts"</a>
Occurs when a sign block is placed in the world.

| Id  | Type     | Name        | Description
| --- | ----     | ----        | -----------
| `0` | `UInt`   | X           | The x coordinate of the block's position.
| `1` | `UInt`   | Y           | The y coordinate of the block's position.
| `2` | `UInt`   | Block Id    | The block id.
| `3` | `String` | Text        | The text.
| `4` | `UInt`   | Sign Type   | The type of the sign.
| `5` | `UInt`   | Player Id   | The id of the player which placed this block.

### <a id="rm-unfavorited">"unfavorited"</a>
Occurs when you un-favorite the world.

### <a id="rm-unliked">"unliked"</a>
Occurs when you un-like the world.

### <a id="rm-unregistercommand">"unregistercommand"</a>
Received once a command is unregistered.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `Boolean` | Success | If the command is successfully removed.
| `1` | `String`  | cmdName/ErrorMsg | Command Name or Error message.

### <a id="rm-updatemeta">"updatemeta"</a>
Occurs when world metadata is updated.

| Id  | Type      | Name           | Description
| --- | ----      | ----           | -----------
| `0` | `String`  | Owner Username | The username of the world owner.
| `1` | `String`  | World Name     | The world name.
| `2` | `Integer` | Plays          | The amount of plays.
| `3` | `Integer` | Favorites      | The amount of favorites.
| `4` | `Integer` | Likes          | The amount of likes.

### <a id="rm-upgrade">"upgrade"</a>
Occurs when the server has updated,

### <a id="rm-worldReleased">"worldReleased"</a>
Occurs when a crew world has been released.

### <a id="rm-wp">"wp"</a>
Occurs when a world portal is placed in the world.
> ID: 374

| Id  | Type     | Name      | Description
| --- | ----     | ----      | -----------
| `0` | `UInt`   | X         | The x coordinate of the block's position.
| `1` | `UInt`   | Y         | The y coordinate of the block's position.
| `2` | `UInt`   | Block Id  | The block id.
| `3` | `String` | Target    | The target of the world portal.
| `4` | `UInt`   | Target Spawn Point | The spawn point to the world.
| `5` | `UInt`   | Player Id | The id of the player which placed this block.

### <a id="rm-write">"write"</a>
Occurs when a non-player message is received (system messages, kicked users)

| Id  | Type     | Name  | Description
| --- | ----     | ----  | -----------
| `0` | `String` | Title | The title of the message.
| `1` | `String` | Text  | The text of the message.

# <a id="send-messages">Send messages</a>

### <a id="sm-access">"access"</a>
Sent to attempt to get edit rights by using the edit key.

| Id  | Type     | Name     | Description
| --- | ----     | ----     | -----------
| `0` | `String` | Edit Key | The edit key.

### <a id="sm-addToCrew">"addToCrew"</a>
Sent to accept adding your world to a crew request.

### <a id="sm-admin">"admin"</a>
Sent to toggle administrator mode.

### <a id="sm-aura">"aura"</a>
Sent to change aura shape and/or color.

| Id  | Type      | Name       | Description
| --- | ----      | ----       | -----------
| `0` | `Integer` | Aura Shape | The aura shape id. *See [Auras](#model-aura)*
| `1` | `Integer` | Aura Color | The aura color id. *See [Aura Colors](#model-aura-color)*

### <a id="sm-autosay">"autosay"</a>
Sent to say an auto-say message.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Auto-Text | The auto-text message id. *See [Auto Text](#model-auto-text).*

### <a id="sm-b">"b"</a>
Sent to place a block in the world.

| Id  | Type      | Name     | Description
| --- | ----      | ----     | -----------
| `0` | `Integer` | Layer    | The layer id. (0 = Foreground, 1 = Background, 2 = Vision Zone, 3 = Tri-Background)
| `1` | `Integer` | X        | The x coordinate of the block's position.
| `2` | `Integer` | Y        | The y coordinate of the block's position.
| `3` | `Integer` | Block Id | The block id.

Additional arguments:

> For sound blocks:

| Id  | Type      | Name     | Description
| --- | ----      | ----     | -----------
| `4` | `Integer` | Sound Id | The sound id.

> For admin label:

| Id  | Type     | Name       | Description
| --- | ----     | ----       | -----------
| `4` | `String` | Text       | The text.
| `5` | `String` | Text Colour | The text colour in Hex.
| `6` | `Integer`| Wrap       | Wrap the text.

> For blocks with a number value:

| Id  | Type      | Name         | Description
| --- | ----      | ----         | -----------
| `4` | `Integer` | Number Value | The number value.

> For portals:

| Id  | Type      | Name            | Description
| --- | ----      | ----            | -----------
| `4` | `Integer` | Portal Rotation | The portal rotation.
| `5` | `Integer` | Portal Id       | The portal id.
| `6` | `Integer` | Portal Target   | The portal target id.

> For world portals:

| Id  | Type     | Name   | Description
| --- | ----     | ----   | -----------
| `4` | `String` | Target | The world portal target.
| `5` | `Integer` | Spawn ID | The world portal spawn id.

> For signs:

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `4` | `String`  | Text      | The text.
| `5` | `Integer` | Sign Type | The sign type.

> For NPC blocks:

| Id  | Type      | Name           | Description
| --- | ----      | ----           | -----------
| `4` | `String`  | Name           | The NPC Name
| `5` | `String`  | First Message  | The first NPC message
| `6` | `String`  | Second Message | The second NPC message
| `7` | `String`  | Third Message  | The third NPC message

> For Coloured blocks:

**How to convert Colour in C#**
https://pastebin.com/WqG5HjUN

| Id  | Type      | Name           | Description
| --- | ----      | ----           | -----------
| `4` | `Uint`    | Colour         | The coloured block in decimal.
| `...` | `Uint` | Rotation | The rotation for spikes.

> For Coloured tri-backgrounds:


| Id  | Type      | Name           | Description
| --- | ----      | ----           | -----------
| `4` | `Uint`    | Rotation       | The rotation of block.
| `5` | `Uint` | Colour | The coloured block in decimal.



### <a id="sm-c">"c"</a>
Sent to collect a coin.

| Id  | Type      | Name       | Description
| --- | ----      | ----       | -----------
| `0` | `Integer` | Gold Coins | The amount of collected gold coins.
| `1` | `Integer` | Blue Coins | The amount of collected blue coins.
| `2` | `UInt`    | X          | The x coordinate of the coin's position.
| `3` | `UInt`    | Y          | The y coordinate of the coin's position.

### <a id="sm-caketouch">"caketouch"</a>
Sent when a cake is touched.

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the cake's position.
| `1` | `UInt` | Y    | The y coordinate of the cake's position.

### <a id="sm-godblock">"godblocktouch"</a>
Sent to enable godmode from block

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the godmode block's position.
| `1` | `UInt` | Y    | The y coordinate of the godmode block's position.

### <a id="sm-checkpoint">"checkpoint"</a>
Sent to change a checkpoint's position.

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the checkpoint's position.
| `1` | `UInt` | Y    | The y coordinate of the checkpoint's position.

### <a id="sm-changeBadge">"changeBadge"</a>
Sent to change the badge.

| Id  | Type     | Name  | Description
| --- | ----     | ----  | -----------
| `0` | `String` | Badge | The badge id. *See [Badges](#model-badges).*

### <a id="sm-clear">"clear"</a>
Sent to clear the world.

### <a id="sm-confirm">"confirm"</a>
Join a friends only or nobody world as staff.

### <a id="sm-crown">"crown"</a>
Sent to collect the gold crown.

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the crown's position.
| `1` | `UInt` | Y    | The y coordinate of the crown's position.

### <a id="sm-death">"death"</a>
Sent to die.

### <a id="sm-diamondtouch">"diamondtouch"</a>
Sent to touch a diamond.

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the diamond's position.
| `1` | `UInt` | Y    | The y coordinate of the diamond's position.

### <a id="sm-effect">"effect"</a>
Sent to activate or deactivate an effect.

| Id  | Type      | Name   | Description
| --- | ----      | ----   | -----------
| `0` | `UInt`    | X      | The x coordinate of the effect's position.
| `1` | `UInt`    | Y      | The y coordinate of the effect's position.
| `2` | `Integer` | Effect | The effect id. *See [Effects](#model-effects).*

### <a id="sm-favorite">"favorite"</a>
Sent to favorite the world.

### <a id="sm-god">"god"</a>
Sent to change the god mode state.

| Id  | Type      | Name     | Description
| --- | ----      | ----     | -----------
| `0` | `Boolean` | God Mode | Value indicating whether the god mode should be enabled.

### <a id="sm-hotbarsmileys">"hotbarSmileys"</a>
Send to set favorite smileys.

| Id  | Type   | Description
| --- | ----   | -----------
| `0-10` | `int` | Add a new favorited smiley.

### <a id="sm-hologramtouch">"hologramtouch"</a>
Sent to touch a hologram.

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the hologram's position.
| `1` | `UInt` | Y    | The y coordinate of the hologram's position.

### <a id="sm-init">"init"</a>
Sent to request the initialization message.

### <a id="sm-init2">"init2"</a>
Sent to request the initialization messages such as [add](#rm-add) and [k](#rm-k) events, etc.

### <a id="sm-key">"key"</a>
Sent to change the edit key.

| Id  | Type     | Name     | Description
| --- | ----     | ----     | -----------
| `0` | `String` | Edit Key | The edit key.

### <a id="sm-kill">"kill"</a>
Sent to kill the world.

### <a id="sm-levelcomplete">"levelcomplete"</a>
Sent to complete the world.

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the trophy's position.
| `1` | `UInt` | Y    | The y coordinate of the trophy's position.

### <a id="sm-like">"like"</a>
Sent to like the world.

### <a id="sm-m">"m"</a>
Sent to move.

| Id   | Type      | Name                 | Description
| ---  | ----      | ----                 | -----------
| `0`  | `Double`  | X                    | The x coordinate of the player's position.
| `1`  | `Double`  | Y                    | The y coordinate of the player's position.
| `2`  | `Double`  | Horizontal Speed     | The horizontal movement speed.
| `3`  | `Double`  | Vertical Speed       | The vertical movement speed.
| `4`  | `Double`  | Horizontal Modifier  | The horizontal movement modifier.
| `5`  | `Double`  | Vertical Modifier    | The vertical movement modifier.
| `6`  | `Integer` | Horizontal Direction | The horizontal movement direction indicator. *(`-1` means left, `1` means right and `0` means that player is not moving horizontally.)*
| `7`  | `Integer` | Vertical Direction   | The vertical movement direction indicator.  *(`-1` means up, `1` means down and `0` means that player is not moving vertically.)*
| `8`  | `Double`  | Gravity Multiplier   | The gravity multiplier.
| `9`  | `Boolean` | Space Pressed        | Value indicating whether the player holds down space-bar.
| `10` | `Boolean` | Space Just Pressed   | Value indicating whether the player has just pressed down space-bar.
| `11` | `Integer` | Tick Id              | The player's current tick id.

#### TIP
If all you want to do is to move the player to a specific block, then you 
can safely ignore most of these parameters and simply send these values:

```
x * 16, y * 16, 0, 0, 0, 0, 0, 0, 0, false, false, 0
```

This will move the player to the block located at the `x` by `y` position.
The other parameters are only useful for more advanced movement code.

### <a id="sm-mod">"mod"</a>
Sent to toggle moderator mode.

### <a id="sm-name">"name"</a>
Sent to change the world name.

| Id  | Type     | Name       | Description
| --- | ----     | ----       | -----------
| `0` | `String` | World Name | The world name.

### <a id="sm-pressKey">"pressKey"</a>
Sent to activate a key.

| Id  | Type      | Name | Description
| --- | ----      | ---- | -----------
| `0` | `Integer` | X    | The x coordinate of the key's position.
| `1` | `Integer` | Y    | The y coordinate of the key's position.
| `2` | `String`  | Key  | The name of the key. *See [Keys](#model-keys).*

### <a id="sm-pm">"pm"</a>
Sending a private message to the player

| Id  | Type      | Name        | Description
| --- | ----      | ----        | -----------
| `0` | `Int`     | Player ID   | The players ID.
| `1` | `String`  | Message     | Message that get sent to the player.

### <a id="sm-ps">"ps"</a>
Sent to change the switch state.

| Id  | Type      | Name        | Description
| --- | ----      | ----        | -----------
| `0` | `UInt`    | X           | The x coordinate of the switch position.
| `1` | `UInt`    | Y           | The y coordinate of the switch position.
| `2` | `UInt`    | Switch Type | The type of the switch. 0 = Purple, 1 = orange.
| `3` | `Integer` | Switch Id   | The switch id.
| `4` | `Boolean` | Enabled     | Value indicating whether the switch is enabled.

### <a id="sm-registercommand">"registercommand"</a>
Sent to server to create a custom slash command
> **NOTE:** This can only be sent by the world owner.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `String`  | cmdName | Command Name.

### <a id="sm-rejectAddToCrew">"rejectAddToCrew"</a>
Sent to reject add to crew request.

### <a id="sm-requestAddToCrew">"requestAddToCrew"</a>
Sent to request adding of the world to a crew.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `String` | Crew Id | The crew id.

### <a id="sm-reset">"reset"</a>
Sent to reset progress.

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the reset block's position.
| `1` | `UInt` | Y    | The y coordinate of the reset block's position.

### <a id="sm-resetCoins">"resetCoins"</a>
Sent to use resetCoins feature.

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the resetCoin block's position.
| `1` | `UInt` | Y    | The y coordinate of the resetCoin block's position.
| `2` | `Boolean` | Coin Type    | True = orange, False = blue coins.

### <a id="sm-say">"say"</a>
Sent to say a chat message.

| Id  | Type     | Name | Description
| --- | ----     | ---- | -----------
| `0` | `String` | Text | The chat message.

> **NOTE:** These can only be sent by the world owner or crew.

### <a id="sm-save">"save"</a>
Sent to save the world.

### <a id="sm-setAllowSpectating">"setAllowSpectating"</a>
Sent to allow or disallow spectating in the world.

| Id  | Type      | Name    | Description
| --- | ----      | ----    | -----------
| `0` | `Boolean` | Allowed | Value indicating whether the spectating should be allowed.

### <a id="sm-setCurseLimit">"setCurseLimit"</a>
Sent to change the curse limit.

| Id  | Type      | Name        | Description
| --- | ----      | ----        | -----------
| `0` | `Integer` | Curse Limit | The curse limit.

### <a id="sm-setHideLobby">"setHideLobby"</a>
Sent to change the world visibility in lobby and profile.

| Id  | Type      | Name   | Description
| --- | ----      | ----   | -----------
| `0` | `Boolean` | Hidden | Value indicating whether the world should be hidden from the lobby and profile.

### <a id="sm-setLobbyPreviewEnabled">"setLobbyPreviewEnabled"</a>
Sent to enable or disable the lobby preview.

| Id  | Type      | Name    | Description
| --- | ----      | ----    | -----------
| `0` | `Boolean` | Enabled | Value indicating whether the lobby preview should be enabled.

### <a id="sm-setMinimapEnabled">"setMinimapEnabled"</a>
Sent to enable or disable the minimap.

| Id  | Type      | Name    | Description
| --- | ----      | ----    | -----------
| `1` | `Boolean` | Enabled | Value indicating whether the minimap should be enabled.

### <a id="sm-setRoomDescription">"setRoomDescription"</a>
Sent to change the world description.

| Id  | Type     | Name        | Description
| --- | ----     | ----        | -----------
| `0` | `String` | Description | The world description.

### <a id="sm-setRoomVisible">"setRoomVisible"</a>
Sent to change the world accessibility.

| Id  | Type      | Name        | Description
| --- | ----      | ----        | -----------
| `0` | `Boolean` | Accessible  | Value indicating whether other players are allowed to join the world.

### <a id="sm-setStatus">"setStatus"</a>
Sent to change the crew world status.

| Id  | Type      | Name        | Description
| --- | ----      | ----        | -----------
| `0` | `Integer` | Crew Status | The crew world status. *See [Crew World Status](#model-crew-status).*

### <a id="sm-setZombieLimit">"setZombieLimit"</a>
Sent to change the zombie limit.

| Id  | Type      | Name         | Description
| --- | ----      | ----         | -----------
| `0` | `Integer` | Zombie Limit | The zombie limit.

### <a id="sm-smiley">"smiley"</a>
Sent to change your smiley.

| Id  | Type      | Name   | Description
| --- | ----      | ----   | -----------
| `0` | `Integer` | Shape  | The smiley shape
| `1` | `Integer` | Colour | The smiley colour
| `2` | `Integer` | Border | The smiley border
| `3` | `Integer` | Eyes   | The smiley eyes
| `4` | `Integer` | Mouth  | The smiley mouth
| `5` | `Integer` | Addon  | The smiley addon
| `6` | `Integer` | Above  | The smiley above
| `7` | `Integer` | Below  | The smiley below
| `8` | `Integer` | Wings  | The smiley wings  

Use this code as example to be able to send different faces:  
[https://pastebin.com/kdZg5rAv](https://pastebin.com/kdZg5rAv)  

### <a id="sm-smileyGoldBorder">"smileyGoldBorder"</a>
Sent to enable or disable the gold smiley border.

| Id  | Type      | Name               | Description
| --- | ----      | ----               | -----------
| `0` | `Boolean` | Gold Smiley Border | Value indicating whether the gold smiley border should be enabled.

### <a id="sm-botwrite">"system"</a>
Use this message to write out * Bot and then a message after as a system message.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `String`  | Message | Message you want to use.

### <a id="sm-team">"team"</a>
Sent to change your team.

| Id  | Type   | Name | Description
| --- | ----   | ---- | -----------
| `0` | `UInt` | X    | The x coordinate of the team block's position.
| `1` | `UInt` | Y    | The y coordinate of the team block's position.

### <a id="sm-time">"time"</a>
Sent to request ["time"](#rm-time) message response.

| Id  | Type     | Name | Description
| --- | ----     | ---- | -----------
| `0` | `Double` | Data | The data to be returned.

### <a id="sm-touch">"touch"</a>
Sent to touch other player transferring effects.

| Id  | Type      | Name      | Description
| --- | ----      | ----      | -----------
| `0` | `Integer` | Player Id | The touched player's id.
| `1` | `Integer` | Effect    | The effect id.

### <a id="sm-unfavorite">"unfavorite"</a>
Sent to un-favorite the world.

### <a id="sm-unlike">"unlike"</a>
Sent to un-like the world.

### <a id="sm-unregistercommand">"unregistercommand"</a>
sent to server to remove a custom slash command
> **NOTE:** This can only be sent by the world owner.

| Id  | Type     | Name    | Description
| --- | ----     | ----    | -----------
| `0` | `String`  | cmdName | Command Name.

# <a id="models">Models</a>

### <a id="model-auto-text">Auto Text</a>
| Hot Key | Message
| ------- | -------
| `0`     | Left
| `1`     | Hi.
| `2`     | Goodbye.
| `3`     | Help me!
| `4`     | Thank you.
| `5`     | Follow me.
| `6`     | Stop!
| `7`     | Yes.
| `8`     | No.
| `9`     | Right.


### <a id="model-badges">Badges</a>


### <a id="model-campaign-status">Campaign Status</a>

| Value | Name
| ----- | ----
| `-1`  | Locked
| `0`   | Unlocked
| `1`   | Completed
| `2`   | Beta Only

### <a id="model-cblocks">Colored blocks</a>
| Name    | ID
| -----   | ----------
| Plain   |  631
| Canvas  |  632
| Checker |  633

### <a id="model-crew-status">Crew World Status</a>

| Value | Name
| ----- | ----
| `0`   | Work in Progress
| `1`   | Open
| `2`   | Released

### <a id="model-effects">Effects</a>
| Value | Image | Effect | BlockID
| ----- | ------ | ------ | ------
| `0`   | ![Jumpeffect](https://github.com/capashaa/EBEProtocol/blob/main/images/417.png) | Jump | 417 |
| `1`   | ![Flyeffect](https://github.com/capashaa/EBEProtocol/blob/main/images/418.png) | Fly | 418 |
| `2`   | ![Speedeffect](https://github.com/capashaa/EBEProtocol/blob/main/images/419.png) | Speed | 419 |
| `3`   | ![Protectioneffect](https://github.com/capashaa/EBEProtocol/blob/main/images/420.png) | Protection | 420 |
| `4`   | ![Curseeffect](https://github.com/capashaa/EBEProtocol/blob/main/images/421.png) | Curse | 421 |
| `5`   | ![Zombieeffect](https://github.com/capashaa/EBEProtocol/blob/main/images/422.png) | Zombie | 422 |
| `6`   | ![Teameffect](https://github.com/capashaa/EBEProtocol/blob/main/images/TeamNone.png) | Team | 423 |
| `7`   | ![LowGravityeffect](https://github.com/capashaa/EBEProtocol/blob/main/images/453.png) | Low Gravity | 453 |
| `8`   | ![FireEffect](https://github.com/capashaa/EBEProtocol/blob/main/images/fire.png) | fire | ... |
| `9`   | ![MultiJumpeffect](https://github.com/capashaa/EBEProtocol/blob/main/images/461.png) | Multi Jump | 461 |
| `10`  | ![Gravityeffect](https://github.com/capashaa/EBEProtocol/blob/main/images/1517.png) | Gravity Effect | 1517 |
| `11`  | ![Poisoneffect](https://github.com/capashaa/EBEProtocol/blob/main/images/poisoneffect.png) | Poison Effect | 1584 |

### <a id="model-keys">Key names</a>
| Image | Value
| ----- | ----------
| ![Keyred](https://github.com/capashaa/EBEProtocol/blob/main/images/6.png) |  red
| ![Keygreen](https://github.com/capashaa/EBEProtocol/blob/main/images/7.png) |  green
| ![Keyblue](https://github.com/capashaa/EBEProtocol/blob/main/images/8.png) |  blue
| ![Keycyan](https://github.com/capashaa/EBEProtocol/blob/main/images/408.png) |  cyan
| ![Keymagenta](https://github.com/capashaa/EBEProtocol/blob/main/images/409.png) |  magenta
| ![Keyyellow](https://github.com/capashaa/EBEProtocol/blob/main/images/410.png) |  yellow

### <a id="model-teams">Teams</a>

| Image | Value | Team Color
| ----- | ----- | ----------
| ![TeamNone](https://github.com/capashaa/EBEProtocol/blob/main/images/TeamNone.png) | `0`   | None
| ![TeamRed](https://github.com/capashaa/EBEProtocol/blob/main/images/TeamRed.png) | `1`   | Red
| ![TeamBlue](https://github.com/capashaa/EBEProtocol/blob/main/images/TeamBlue.png) | `2`   | Blue
| ![TeamGreen](https://github.com/capashaa/EBEProtocol/blob/main/images/TeamGreen.png) | `3`   | Green
| ![TeamCyan](https://github.com/capashaa/EBEProtocol/blob/main/images/TeamCyan.png) | `4`   | Cyan
| ![TeamMagenta](https://github.com/capashaa/EBEProtocol/blob/main/images/TeamMagenta.png) | `5`   | Magenta
| ![TeamYellow](https://github.com/capashaa/EBEProtocol/blob/main/images/TeamYellow.png) | `6`   | Yellow

### <a id="model-aura">Aura</a>

| Id | Name  
| ---- | ----- |
| `0`   | `Default`  
| `1`   | `Pinwheel`
| `2`   | `Torus`
| `3`   | `Ornate`
| `4`   | `Spiral`
| `5`   | `Star`
| `6`   | `Snowflake`
| `7`   | `Atom`
| `8`   | `Sawblade`
| `9`   | `Target`
| `10`  | `Bubble`
| `11`  | `Galaxy`
| `12`  | `Heart`
| `13`  | `Flower`

### <a id="model-aura-color">Aura Color</a>

|  Id | Name
| ---- | ----- |
| `0`   | `White`
| `1`   | `Red`
| `2`   | `Blue`
| `3`   | `Yellow`
| `4`   | `Green`
| `5`   | `Purple`
| `6`   | `Orange`
| `7`   | `Cyan`
| `8`   | `Gold`
| `9`   | `Pink`
| `10`  | `Indigo`
| `11`  | `Lime`
| `12`  | `Black`
| `13`  | `Teal`
| `14`  | `Gray`
| `15`  | `Amaranth`
| `16`  | `Brown`  
| `17`  | `Peach`


### <a id="model-npcid">NPC</a>

| NPC Picture  | NPC Name | NPC Block ID
| ---- | ----- | ----------
| ![smile](https://github.com/capashaa/EBEProtocol/blob/main/images/npcHappy.png)  | `Smile`   | `1550`
| ![sad](https://github.com/capashaa/EBEProtocol/blob/main/images/npcSad.png)   | `Sad` | `1551`
| ![old](https://github.com/capashaa/EBEProtocol/blob/main/images/npcOld.png)   | `Old` | `1552`
| ![angry](https://github.com/capashaa/EBEProtocol/blob/main/images/npcAngry.png)   | `Angry` | `1553`
| ![slime](https://github.com/capashaa/EBEProtocol/blob/main/images/npcSlimey.png)   | `Slime` | `1554`
| ![robot](https://github.com/capashaa/EBEProtocol/blob/main/images/npcRobot.png)   | `Robot` | `1555`
| ![knight](https://github.com/capashaa/EBEProtocol/blob/main/images/npcKnight.png)   | `Knight` | `1556`
| ![meh](https://github.com/capashaa/EBEProtocol/blob/main/images/npcMeh.png)   | `Meh` | `1557`
| ![cow](https://github.com/capashaa/EBEProtocol/blob/main/images/npcCow.png)   | `Cow` | `1558`
| ![frog](https://github.com/capashaa/EBEProtocol/blob/main/images/npcFrog.png)   | `Frog` | `1559`
| ![bruce](https://github.com/capashaa/EBEProtocol/blob/main/images/npcBruce.png)   | `Bruce` | `1570`
| ![starfish](https://github.com/capashaa/EBEProtocol/blob/main/images/npcStarfish.png)   | `Starfish` | `1569`
| ![computer](https://github.com/capashaa/EBEProtocol/blob/main/images/npcComputer.png)   | `Computer` | `1571`
| ![skeleton](https://github.com/capashaa/EBEProtocol/blob/main/images/npcskeleton.png)   | `Skeleton` | `1572`
| ![zombie](https://github.com/capashaa/EBEProtocol/blob/main/images/npczombie.png)   | `Zombie` | `1573`
| ![ghost](https://github.com/capashaa/EBEProtocol/blob/main/images/npcghost.png)   | `Ghost` | `1574`
| ![astronaut](https://github.com/capashaa/EBEProtocol/blob/main/images/npcastro.png)   | `Astronaut` | `1575`
| ![santa](https://github.com/capashaa/EBEProtocol/blob/main/images/npcsanta.png)   | `Santa` | `1576`
| ![snowman](https://github.com/capashaa/EBEProtocol/blob/main/images/npcsnowman.png)   | `Snowman` | `1577`
| ![walrus](https://github.com/capashaa/EBEProtocol/blob/main/images/npcwalrus.png)   | `Walrus` | `1578`
| ![crab](https://github.com/capashaa/EBEProtocol/blob/main/images/npcCrab.png)   | `Crab` | `1579`
