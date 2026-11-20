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

## How it works

- Eat orbs to grow; new segments are Spitters (auto-fire) or Spikes (contact damage). Three Spikes in a row fuse into a Mace.
- Level up for cards, kill the rival snakes, survive until the mini-boss arrives at 3:00 and kill it to win.
- The arena edge, the boss and its walls are deadly.
- All tunables live in the `CONFIG` object at the top of the script.

## Rebuilding the APK

The APK is a minimal Android WebView app (`MainActivity.java` + manifest) with `index.html` bundled as an asset.
Build tools are not included in this repo.
