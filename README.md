# List of all my WeakAura's for Dragonflight
**Here I will post helpful macro's that you can use in-game for general gameplay or gold making.**

![YouTube Channel Subscribers](https://img.shields.io/youtube/channel/subscribers/UCY_LsfkMQS--TVMvGl90rNA?style=social)
![Twitch Status](https://img.shields.io/twitch/status/xscarlife?style=social)
## General

**3 mounts in one: This macro will let you cast one of the mounts that you add in the macro.**
```
#showtooltip
/cast [btn:3] Grand Expedition Yak
/cast [btn:2] Azure Water Strider
/cast X-53 Touring Rocket
```

**Mountspecial: This one will do a mountspecial on your mount.**
```
/mountspecial
```

**Reset Instance: This will reset the instance by clicking the macro.**
```
/script ResetInstances();
```

**Leave party: By pressing this macro you will leave the group directly.**
```
/script C_PartyInfo.LeaveParty()
```

## Gold Making

**Pull Timer: This macro will start a pull timer for you so you know when to stop killing mobs and start to loot them. Adjust the time to your liking.**
```
/sw 01:40
/sw play
```

**Delete items: This will delete all items at once containing the word 'fang'. You can replace the word 'fang' with the item you want to destroy in your bags.**
```
/run for bag = 0,4,1 do for slot = 1, 32, 1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Fang") then PickupContainerItem(bag,slot); DeleteCursorItem(); end; end; end
```

**Disenchant: This one can be used to disenchant a certain item by clicking the macro button. Replace the 'Aspirant's Staff of Grace' by the item you want to disenchant.**
```
/cast Disenchant
/use Aspirant's Staff of Grace
```

**Equip Fishing: This will equip your fishing pole & fishing hat at once. Replace the fishing pole and hat with the one you own.**
```
/Equip Underlight Angler
/Equip Weather-Beaten Fishing Hat
/use Weather-Beaten Fishing Hat
```

## Fury Warrior

**Cancel Bladestorm Macro. This macro allows you to cancel your Bladestorm early. You cannot cast other abilities while Bladestorming, so this can be useful if targets die during the channel.**
```
#showtooltip Bladestorm
/cancelaura Bladestorm
/cast Bladestorm
```

**Pummel Macro. This macro uses Pummel against your focus target, if you have one, or against your current target if you have no focus target.**
```
#showtooltip Pummel
/cast [@focus, harm, exists][@target] Pummel
```

**Automatic Heroic Leap. This will cast Heroic Leap where ever your cursor is located, without waiting for the targeting circle.**
```
#showtooltip Heroic Leap
/cast [@cursor] Heroic Leap
```

**Charge and Victory Rush. Because Charge is off the Global Cooldown, Victory Rush or any other melee ability can be used on the same keybind. When outside of melee range, Charge will be cast instead.**
```
#showtooltip
/cast Charge
/cast Victory Rush
```
