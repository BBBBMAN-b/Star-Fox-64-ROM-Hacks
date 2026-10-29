# Custom Fox 64

A Star Fox 64 mod with an in-game cheat menu, playable ships from across the series, two new difficulties, and a long list of game-mode options. Built on the [sf64 decompilation](https://github.com/sonicdcer/sf64).

**Version:** 19.2

## What you need

- A **Star Fox 64 (USA) Rev 1** ROM in big-endian `.z64` format. This repository does not include the game, so you need your own copy.
  - SHA-1: `09f0d105f476b00efa5303a3ebc42e60a7753b7a`
  - MD5: `741a94eee093c4c8684e66b89f8685e8`
- An emulator with **Expansion Pak (8 MB)** support. gopher64 is recommended. Ship Swap, the Omega Laser and Double/Triple Enemies need the Expansion Pak.
- A BPS patcher, for example [Floating IPS (Flips)](https://github.com/Alcaro/Flips) or the [ROM Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) website.

> Heavy options such as Triple Enemies are built for emulators. They may run slowly on original N64 hardware.

## How to install

1. Open your patcher.
2. Pick `Custom_Fox_64_v19.2.bps` as the patch and your Star Fox 64 (USA) Rev 1 ROM as the file to patch.
3. Save the patched ROM and load it in your emulator with the Expansion Pak turned on.

On the main menu, the new **Custom Fox 64** option opens the Cheats, Ship Swap and Misc pages.

## Unlocking things

Everything except the Arwing, Skip Cutscenes and the Unlock All cheat starts locked. Locked entries are grayed out and show how to unlock them. Turning on **Unlock All** opens everything right away.

| Unlock | How |
|---|---|
| All cheats | Beat Andross on Normal |
| Vehicle Upgrades | Beat Andross on Normal |
| Master difficulty | Beat Andross on Expert |
| Andross's Revenge, Double Enemies | Beat Andross on Master |
| Triple Enemies | Beat Andross on Andross's Revenge |
| Choose Any Path | Clear every mission on Normal |
| Arwing MK2 | Beat Andross on Expert |
| Great Fox | Beat Andross on Andross's Revenge |
| Wolfen / Wolfen MK2 | Shoot down all of Star Wolf on Fortuna (Normal / Expert) |
| Katt's Fighter / MK2 | Clear Zoness, where Katt first shows up (Normal / Expert) |
| Bill's Fighter / MK2 | Save the Katina base with Bill (Normal / Expert) |

A clear on a harder difficulty also counts for the easier ones, and Master and Andross's Revenge count as Expert.

## Cheats

Infinite bombs, lives, health and boost/brake. No clip. Max laser. Ally infinite health, ally no clip and ally level 3 lasers. Start with 150 hits, max hits (the hit counter goes up to 9999). Always-charged laser, rapid-fire charged laser, and rapid fire with auto charge. Bomb blasts 4x the area. 2x or 4x damage. Multi-lock for 3, 5, 7 or 12 enemies. Katt and Bill upgrade. Collect all items. Unlock All.

## Ship Swap

| Ship | Abilities |
|---|---|
| Arwing | The standard ship |
| Arwing MK2 | 2x health, 3-hit shield, green, blue and gold lasers, locks 3 targets, a new bomb every 8 seconds... and a secret |
| Wolfen | Single red lasers |
| Wolfen MK2 | 2-hit shield that recharges after 5 seconds, twin green, orange and red lasers |
| Katt's Fighter | Standard lasers |
| Katt's Fighter MK2 | Pink hyper lasers do 2x damage, and every barrel roll restores 5% health |
| Bill's Fighter | Standard lasers |
| Bill's Fighter MK2 | Takes half damage, yellow hyper lasers, a new bomb every 10 seconds |
| Great Fox | 2x health, 12-hit shield, a big C-Left beam, auto lock on 5 targets, picks up items you fly near |

## Misc: game modes

- **Master:** a new difficulty after Expert. You take 2x damage, allies never fall and fire level 3 lasers, and bosses have 2x health with shields. Enemies and bosses shoot more often and their shots are faster.
- **Andross's Revenge:** you take 4x damage, bosses have 5x health with 4 shields, barrel rolls make you invincible, you get 3 green shields that recharge after 10 seconds, and Triple Enemies is always on. Enemies fire bursts of 3 and fly more aggressively, bosses attack twice as often, and Andross's eyes grow back. The Arwing MK2 is recommended.
- **Double Enemies / Triple Enemies:** every enemy that can be hit appears 2 or 3 times. Bosses, Star Wolf and the Macbeth train are left alone.
- **Vehicle Upgrades:** the Blue Marine gets rapid-fire lasers, holds B for torpedoes that travel faster and have a 4x blast, and locks on to 3 targets. The Landmaster gets a new bomb every 10 seconds.
- **Skip Cutscenes:** START skips mission intros and endings. START also skips the end credits.
- **Choose Any Path:** after a mission, press left or right on the D-pad to pick any route on the map.

## Building from source

`Custom_Fox_64_v19.2_decomp.patch` holds every source change, made against sf64 decomp commit `4235c59`. Set up the decomp with your own ROM by following its instructions, then:

```
git checkout 4235c59
git apply Custom_Fox_64_v19.2_decomp.patch
make COMPARE=0
```

The ROM must then be compressed and its checksum fixed. The decomp's `tools/comptool.py` does both.
