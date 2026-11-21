# VRadical Stories registry

This repository is the public registry of interactive **VRadical Stories**:
branching VR180 videos authored in VRadical Studio and played in VRadical
Player. It contains no video. It only links the videos published on DeoVR or
YouTube to their story companion (the description of the nodes, choices and
menus), so that VRadical Player can turn an ordinary online video into the
interactive story.

VRadical Studio writes to this repository automatically when a story export
is published. Please do not edit these files by hand.

## Contents

- `index.json`: one entry per published revision of a story, with the
  DeoVR/YouTube video ids of that revision (format `vradical-story-index`,
  version 1).
- `stories/<story id>/r<revision>.json`: the story companion of each
  revision. A published companion is never replaced; a new export is a new
  revision.

Each index entry records the SHA-256 of its companion. The player checks it,
then checks the companion against the video it is playing, and ignores
anything that does not match.
