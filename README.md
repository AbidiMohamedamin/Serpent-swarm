# Serpent Swarm

A 2D top-down survival game where every segment of your snake is an auto-firing weapon.
One self-contained HTML file: plain JavaScript and Canvas 2D, no libraries, no external assets.
Music and sound effects are synthesized live with WebAudio.

## Play

- **Browser:** open `index.html` (or host it on GitHub Pages).
- **Android:** install `serpent-swarm.apk` (allow "install unknown apps"). It is a WebView wrapper around the same game.

## Controls

| Action | Keyboard | Gamepad | Touch |
|---|---|---|---|
| Steer | WASD / arrows | left stick / d-pad | drag anywhere |
| Shed tail (bomb) | Space | A | SHED button |
| Laser (costs 2 segments) | E | X | LASER button |
| Pause | Esc / P | Start | pause button |
| How to play | H | Y | menu |
| Mute / fullscreen | M / F | | |
| Watch the bot play | B | | menu |

## Modes

Open SELECT MODE on the title screen to see every mode with its rules and your best score, then pick one to play. Records are saved per mode.

| Mode | What changes |
|---|---|
| Classic | Survive 3:00, then kill the mini-boss. |
| Boss Rush | Start with 14 segments, boss at 1:00 with less health. |
| Endless | No boss; the swarm keeps ramping. Survival time adds to your score. |
| Laser Duel | Two bosses from the first seconds, no swarm and no rivals. The laser is free (no segments lost) with a 1.4 s cooldown. Kill both to win; faster wins score more. |
| Rival Hunt | No swarm, no boss, no Spitters or Spikes and no shed. Hunt 5 armoured, deadly rival snakes (touch one and you die): only the laser (costs 1 segment) hurts them, and they eat the orbs that rain on the arena and grow longer. One of them is an orange BRUTE: slow, huge, tough, never dodges, counts as 2 kills. |
| Hard | Tougher swarm, rivals from 0:12, a faster and tougher boss. |

Modes are CONFIG overrides: add an entry to the `MODES` array near the top of the script.

## Experiments

New ideas live on the `experiments` branch (cone laser, boss health bar, laser-only growing rivals, ...). `main` stays the stable, shareable version.

## How it works

- Eat orbs to grow; new segments are Spitters (auto-fire) or Spikes (contact damage). Three Spikes in a row fuse into a Mace.
- Level up for cards, kill the rival snakes, survive until the mini-boss arrives at 3:00 and kill it to win.
- The arena edge, the boss and its walls are deadly.
- All tunables live in the `CONFIG` object at the top of the script.

## Rebuilding the APK

The APK is a minimal Android WebView app (`MainActivity.java` + manifest) with `index.html` bundled as an asset.
Build tools are not included in this repo.








