# scoop-music

A [Scoop](https://scoop.sh) bucket for music production, MIDI and audio tooling on Windows.

It deliberately **does not duplicate** what the official `extras` bucket already ships. Audacity, REAPER, MuseScore, LMMS, OpenMPT, Furnace, MilkyTracker, Schism Tracker, Pure Data, plugdata, Sonic Pi, Surge, TuxGuitar, Sonic Visualiser, Praat, MusicBrainz Picard, Spek, ocenaudio, FamiStudio, OpenUtau and fluidsynth are all in `extras` — install those from there.

## Install

```bash
scoop bucket add music https://github.com/USERNAME/scoop-music
```

```bash
scoop install music/showmidi
```

## Apps

### Portable — extract and run, no system changes

| App | Description |
|---|---|
| `showmidi` | Real-time MIDI monitor, visualizes activity per channel. Standalone + VST3/CLAP |
| `sendmidi` | CLI tool for sending MIDI messages |
| `receivemidi` | CLI tool for monitoring and logging incoming MIDI |
| `cardinal` | Virtual modular synth, a VCV Rack fork with ~2000 modules bundled (~1.1 GB) |
| `vcv-rack` | VCV Rack Free, virtual Eurorack modular synthesizer |
| `dexed` | Yamaha DX7 FM synthesizer emulation |
| `supercollider` | Audio synthesis and algorithmic composition platform |
| `bespoke-synth` | Modular DAW with a live-patchable node workflow |
| `frescobaldi` | Sheet-music editor for LilyPond (pair with `main/lilypond`) |
| `polyphone` | SoundFont editor for sf2 / sf3 / sfz |
| `mixxx` | DJ software with 4 decks, beatgrids and controller support |
| `sunvox` | Modular synthesizer with a pattern-based tracker sequencer |
| `bambootracker` | Tracker for the Yamaha YM2608 (OPNA) chip |
| `klystrack` | Chiptune tracker with a built-in synth engine |

### Runs a vendor installer

These download and verify the vendor's own installer, then run it. They install outside the Scoop directory, so `scoop uninstall` will not fully remove them.

| App | Description |
|---|---|
| `midieditor` | MIDI file editor with piano-roll editing (interactive setup) |
| `ultimate-vocal-remover` | AI stem separation; downloads models on first run |
| `rew` | Room EQ Wizard — acoustic measurement and EQ design |
| `zrythm` | Automated DAW, freely downloadable trial build |

### Audio drivers — read this first

These install **system-level audio drivers**. They require administrator rights, most require a reboot, and Scoop cannot meaningfully track or roll back driver state.

**Uninstall them through Windows "Apps & features", not `scoop uninstall`.**

| App | Description |
|---|---|
| `asio4all` | Universal ASIO driver for WDM devices |
| `flexasio` | Universal ASIO driver built on PortAudio |
| `vb-cable` | Virtual audio cable, routes app output to a recordable input |
| `voicemeeter` | Virtual audio mixer and routing console |
| `loopmidi` | Virtual loopback MIDI ports for routing MIDI between apps |
| `equalizerapo` | System-wide parametric EQ as an Audio Processing Object |

## Notes

- Every manifest pins a SHA-256 hash and carries `checkver` + `autoupdate`, so the included Excavator workflow can keep versions current.
- Licensing is the user's responsibility. `zrythm` is a trial build; `vb-cable` and `voicemeeter` are donationware.
- FL Studio, Bitwig and other commercial DAWs are not included, but their installers are versioned and could be added.

## License

Manifests are MIT licensed. The packaged applications carry their own licenses.
