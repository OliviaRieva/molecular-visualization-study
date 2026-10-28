# Study notes

## Purpose

This case study records a visual quality-assurance pass across two representations produced by a private collaborative molecular-visualization workflow:

1. a fast terminal-driven preview, including a rotating GIF; and
2. a higher-fidelity Blender render.

The comparison is about communication and usability, not quantum-chemical validation.

## Test matrix

| ID | Structure class | Stress case | Preview check | Blender check | Outcome |
|---|---|---|---|---|---|
| P01 | Small, mostly planar molecule | Aromatic ring and substituents | Bond topology remains legible | Camera preserves the molecular skeleton | Both views useful; preview is clearer for a quick bond scan |
| A01 | Compact non-planar molecule | Projection overlap | Rotation resolves ambiguous overlap | Depth cues separate atom positions | Turntable is important before judging a single frame |
| C01 | Long chain | Extreme aspect ratio | Structure fits without clipping | Camera does not collapse the chain edge-on | Geometry-aware framing improves repeatability |
| X01 | Periodic crystal model | Repetition and unit-cell context | Axes and cell remain visible | Repeated structure reads spatially | Beauty render should accompany, not replace, cell-aware plots |

## Review checklist used

- Is the complete structure visible?
- Are atoms or bonds clipped by the frame?
- Does projection create misleading overlap?
- Are element colors distinguishable against the background?
- Are thin bonds still visible at README-scale display?
- Does lighting imply depth without hiding topology?
- For periodic material, is the unit-cell context preserved somewhere?
- Can a repeated run produce a comparable camera orientation?

## Interpretation boundary

The renders should be read as views of supplied geometry. They do not establish:

- energetic stability;
- a lowest-energy conformer;
- correct charge or protonation state;
- bond order accuracy in every input format;
- electron density, orbitals, spectra, or reaction behavior.

Those questions require separate computational or experimental evidence.

## Reproducibility note

The underlying renderer belongs to a private MQS collaboration and is not released here. This public repository therefore preserves the test set, observations, and visual outputs rather than claiming to be a reproducible software release.

