# Masked

Masked is a data pack with its resource pack built in. It adds the Masked origin to the Origins layer: people of the jungle who slip through the canopy behind a carved wooden mask, with a parrot on their shoulder keeping watch. Every power is built from Apoli JSON, with no commands and no Java.

This is a rebuild of InkBat's Masked origin for Apoli and Origins. The idea is InkBat's; the powers, the mask model, its textures and the text in this pack are new.

## Requirements

- Apoli 1.130.0 or newer and Origins 1.52.0 or newer
- Fabric 1.20.1, Fabric 1.21.1 or NeoForge 1.21.1

Put the folder (or a zip of it) in the world's `datapacks` folder and in your `resourcepacks` folder. The resource half carries the mask model, the view through the mask, the icons and all of the text.

## Keys

| Power | Key |
|---|---|
| The Mask | The Origins primary key, G unless you changed it |
| Cape Landing | Sneak in mid-air |

The Origins screen shows each key on the power's badge, using the keys you have bound.

## Powers

| Power | What it does |
|---|---|
| The Mask | Puts your carved mask on or takes it off. Other players see it on your face, and you see the world through its eye holes. |
| Within the Trees | While masked you pass through logs, leaves, vines, ladders and bamboo, and sneaking on top of them sinks you down through. You run 40% faster, hit 3 points harder, take a fifth less damage, shrug off 40% of knockback, jump higher and take a tenth of the usual fall damage. A green haze limits how far you can see. |
| Jungle Companion | Your tamed parrots can fly through the canopy and never suffocate inside it. While one rides on your shoulder and your mask is on, the haze lifts, you see in the dark and monsters within 24 blocks glow red. |
| Cape Landing | While you wear a leather tunic, sneak in mid-air to throw your cape open. You drift down slowly with your arms spread, land without harm, and the cape needs three seconds to fold back up. |
| Warping Shadow | Bolts you fire from a crossbow in your offhand carry your shadow. Wherever the first of them lands, in a wall, on the ground or in a creature, you step out of it. |
| Anthropophobia | Without your mask you can't eat, and your health doesn't come back on its own. With another player within 7 blocks, your cape and your shadow fail you three times in ten. |
| Fear of the Flames | Fire, lava, magma, lightning, explosions and fireworks hurt you twice as much. |
| Armor Restrictions | The mask leaves no room for a helmet, and nothing heavier than iron fits you. |
| Jungle Inhabitant | You first wake up in a jungle, and you return to one whenever you die without a bed. |

## The parrot

Every parrot carries a small hidden power from this pack. It only does anything for parrots tamed by a Masked player: those can fly through logs, leaves and the rest of the canopy, and they can't take suffocation damage. A parrot that hops off your shoulder while you are deep inside a tree ends up inside the logs with you and flies back out on its own.

Parrot sight only counts parrots riding on your shoulders. It updates the moment a parrot lands on you or hops off.

## Coming from InkBat's version

- The origin is `masked:masked` and every power uses the `masked` namespace. Old origin choices don't carry over.
- The mask is a model drawn on your face. It no longer takes a player head into your helmet slot, and taking it off can't delete a helmet.
- The masked bonuses are attributes and powers. There are no hidden potion effects for milk to clear, and blindness no longer stops you from sprinting.
- A parrot on either shoulder counts, where the old version only checked the left one.
- Warping Shadow follows the bolt itself, so it works with tipped arrows, Multishot and Piercing, and it sets you down clear of the wall the bolt hit.
- Fear of the Flames now covers lightning and explosions, which the old version misspelled or left out.
- Anthropophobia only checks for other players at the moment you open your cape or a bolt lands.

## Layout

Each visible power has a file named after it in `data/masked/powers/`, and everything that power uses sits in a folder of the same name, such as `the_mask/model.json` or `cape_landing/drift.json`. The parrot powers are in `jungle_companion/parrot/` and reach every parrot through `data/masked/global_powers/parrots.json`. The canopy blocks are the block tag `masked:canopy` and the monsters that glow are the entity tag `masked:jungle_companion/dangers`, each written for both 1.20.1 and 1.21.1 folder names. The mask model is `assets/masked/geo/the_mask.geo.json`.
