# Adventures with Anxiety *the super cool awesome* NES port
An open source fan port of Nicky Case's [*Adventures with Anxiety*](https://ncase.me/anxiety/)
([source](https://github.com/ncase/anxiety)) to the Nintendo Entertainment System.

It runs on an MMC3 cartridge. The scripts are compiled to bytecode for a small 6502 virtual
machine, every picture and animation is converted to NES tiles, and the soundtrack has been
re-composed into 2A03 tracker music.

Your progress (whatever act you reached) and the options are saved into the battery RAM.

![rooftop](https://file.garden/aejaU8l_-hvXF5j_/act3-rooftop.png) ![fight](https://file.garden/aejaU8l_-hvXF5j_/act1-fight.png) ![party](https://file.garden/aejaU8l_-hvXF5j_/act2-party.png)

## Download
Two ROM files are in [`releases/`](releases/). Both play the exact same way, but they only differ in how the picture changes are shown.

| ROM | CHR-RAM | Picture changes | Runs on |
|---|---|---|---|
| [`anxiety-32kb.nes`](releases/anxiety-nes-v2-32kb-chr.nes) **(recommended)** | 32 KB | Instant: the next picture is built off-screen and swapped in within one frame | Emulators (Mesen, FCEUX, Nestopia…), flash carts / repro boards with 32 KB CHR-RAM |
| [`anxiety-8kb.nes`](releases/anxiety-nes-v1-8kb-chr.nes) | 8 KB | Streamed: big changes build up over several frames, block by block | Any MMC3 setup, including a stock TGROM-style 8 KB CHR-RAM board |

## Music
If you would like to listen to the tracker files alone they are located in [`tracker/`](tracker/)
They should be compatible with *most* tracking software although, I reccomend [Dn-Famitracker](https://github.com/Dn-Programming-Core-Management/Dn-FamiTracker).

## Building
not avaliable yet soz T-T

## Hardware notes
- Mapper 4 (MMC3), w/ NES 2.0 header.
- 512 KB PRG-ROM, 8 KB battery PRG-RAM.
- CHR-RAM: 32 KB in v2, 8 KB in v1.
- Screen layout: picture area on rows 1–18, text box on rows 19–28.
- v2 uses four raster IRQ splits per frame (three picture windows plus the text window).

## Credits and licences
- **Original game:** *Adventures with Anxiety*, a game by [Nicky Case](https://ncase.me)
- **Original music:** [Monplaisir](https://loyaltyfreakmusic.com).
- **Tracker covers:** [Me](https://niko.horse/)  `¯\_⁽ツ⁾_/¯`
- **Sound effects** Originated from [FreeSound.org](https://freesound.org/).
- This port is an unofficial fan project, not affiliated with Nicky Case.
