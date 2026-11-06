# Origami tools

Small, free tools for game-development workflows. Both run locally without a tool account or upload service.

## Animation Segment Transfer for Godot

**Merge selected scalar property keys between animation clips without copying whole tracks.** Preview the exact paths and inclusive range, keep the original times, and use Godot's normal Undo/Redo. Collisions are refused rather than overwriting destination keys.

[Download the add-on or runnable demo](https://github.com/jshms7/animation-segment-transfer/releases/tag/v0.1.0) · [Instructions and full limits](https://github.com/jshms7/animation-segment-transfer)

1. Extract the demo ZIP and open `project.godot` in Godot 4.7.2. For an existing project, install the add-on ZIP and enable the plugin instead.
2. Select an AnimationPlayer, choose source and destination clips, check tracks and set the range. Click **Preview**.
3. Click **Transfer**, inspect the destination timeline, then undo or save. The README includes a three-key worked example.

![Segment Transfer's three-key preview in Godot.](https://raw.githubusercontent.com/jshms7/animation-segment-transfer/bcd247f551076c88696cc7810923e55f6f04a342/docs/images/three-key-preview.png)

Supports bool, int and float Value tracks in independent local scene-embedded clips. No vectors, transforms, imported clips, retiming or path remapping. Tested in Godot 4.7.2 on Linux. MIT licensed; offline, no telemetry.

## PNG ORM Packer v0.2

**Batch ambient occlusion, roughness and metallic masks into exact numeric ORM PNGs.** Review filenames and exceptions, then download one image per successful material plus a text report. Failed sets leave Ready; correct the files and select them again to retry.

[Open the browser tool](https://jshms7.github.io/png-orm-packer/texture-batch.html) · [Download v0.2.0 and examples](https://github.com/jshms7/png-orm-packer/releases/tag/v0.2.0) · [Source and full limits](https://github.com/jshms7/png-orm-packer#format-and-batch-limits)

1. Extract `png-orm-packer.zip` and open `texture-batch.html` in desktop Chrome or Firefox.
2. Choose all six files in `examples/`, review the two sets, then click **Pack ready sets**.
3. Click **Download packed ZIP**. It contains `stone_orm.png`, `wood_orm.png` and the report.

![PNG ORM Packer with a real CC0 material prepared as 8-bit PNG.](https://raw.githubusercontent.com/jshms7/png-orm-packer/f7d9fd24b5e215a78544bd29d0e78340d1d74999/screenshot.png)

Output: **R = AO, G = roughness, B = metallic, A = 255**. Each value comes from its input's red channel; optional inversion uses `255 - roughness`. No colour correction, resizing or source-file changes.

Supports matching 8-bit, non-interlaced grayscale/RGB/grayscale-alpha/RGBA PNGs. Palette, 16-bit and animated PNGs are refused. Per input: up to 4096 × 4096 pixels and 32 MiB; selection/output/browser-memory limits also apply. Full limits and hosting privacy details are in the README. Unlicense; no installation or tracking in the local tool.

Screenshots show our own checks, not customer results. The texture screenshot uses a separately prepared [CC0 Poly Haven material](https://polyhaven.com/a/metal_plate), not bundled customer files. GitHub's own privacy terms apply to hosted pages and downloads.
