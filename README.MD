<img src=http://u.cubeupload.com/Owyn/lilbaha.jpg>

# pet-skin-replacer
Customize your pet's appearance

## Info
- Creatures not used as pets normally have collision, to avoid bumping into them in combat use `pets stay` option (then even using Leaping Strike right into pet's face won't hinder your movement)   
- Feel free to use info in `DC` folder to find more `huntingZoneId` and `templateId` to set from any existing creatures out there  
- Module is client-side only, that means only you can see the difference. Nobody else can see your new pet.	

## Usage
### `pets`
- Toggle on/off
### `pets ?`
- Outputs a list of available pet presets
### `pets set [preset_name]`
- Set your pet from a preset. (Example: `pets set felicity` will make your pet into a white cat with a flower on its head!)
### `pets setid [huntingZoneId] [templateId]`
- Set your pet from any NPC model. You need to know the templateId and huntingZoneId though. (eg `pets set id 983 950` to summon goddess Velik herself from the very heavens)
### `pets save`
- Saves current pet configuration into a per-character savefile which would get loaded next time you login onto this character
### `pets reload`
- Reloads current pet configuration from a per-character savefile (or resets to default if it doesn't exist)
### `pets size [size]`
- Sets pet size (eg `pets size 1.5` to make it 50% bigger or `0.1` to make it 10x times smaller)
### `pets name [name]`
- Sets pet name to one specified
### `pets move [number]`
- Set movement type for your pet (some NPCs and monsters might have multiple types of animations you can choose from):
```
-1 = copy players movetype (eg jump when you jump etc) (works only with "pet stay" option enabled),
0 = running, 1 = walking, 2 = falling, 5 = jumping,
6 = jump intersection and end when something is blocking the path and the player can't travel in the X and Y axis
7 = stop moving, landing, 8 = swimming, 9 = stop swimming, 10 = falling after jumping
```
### `pet stay [degrees] [distance]`
- Set pet to stay near you at [distance] units away at [degrees] degrees (eg `90` degrees - is at right, `-90` is at left, `180` is in the back)
### `pet play [animation]`
- Plays a custom animation on the pet (eg `pets play death`), animations are listed in the DataCenter files
### `pet anim [animation] [newAnimation] [loopDuration]`
- Set a pet to play custom animation instead of existing ones (eg `pets anim run walk 988` to set a new running animation to be the same as walking one with the repeat loop timing of 998 milliseconds), [loopDuration] argument is only needed for `run` and `walk` animations list of replacable animations:  
```
jump
spawn
death		(when pet disappears)
skill		(when pet uses his power buff skill on you)
unarmedwait	(pose for when custom run or walk animations should end too soon)
walk		(partners are unable to walk unless you set them this custom animation)
run			(non-partner pets can only use walk animation unless you set them this custom animation)
```


## Presets
Note: Only monsters have collision hitboxes

| Partners | Rare Pets      | Critters | Usual Pets | Monsters     |
|:---------|:---------------|:---------|:-----------|:-------------|
| Loo      | Mushroom       | Bunny    | Pixie      | Pooky        |
| Mary     | Slime          | Puppy    | Miss Kitty | Tuwangi      |
| Kuncun   | Cat            | Dog      | Juicy      | Mewy         |
| Cocomin  | Hanami         | Goat     | Candy      | Dahlia       |
|          | Baldi          | Pig      | Prince     | Pumpkin      |
|          | Durion         | Rooster  |            | Bandersnatch |
|          | Sheep          | Pidgeon  |            | Lilith       |
|          | Felicity       | Mystel   |            | Bahaar       |
|          | Moon Bunny     | Okami    |            | Imperator    |
|          | Miss Katonic   |          |            | Darkan       |
|          |                |          |            | Kylos        |
|          |                |          |            | Lizard       |
|          |                |          |            | Lumikan      |
|          |                |          |            |              |

<img src=http://u.cubeupload.com/Owyn/petspreview.jpg>


## Changelog:
- 07.07.19: added custom animations, also added those into `Bahaar`, `Lilith` and `Okami` (wandering god Halrath) presets (reload the preset via eg `pets set Okami`), please enjoy those, and say if you have a favorite pet model you'd want animations for in issues (animations are listed inside `AnimationData.json` DC file)