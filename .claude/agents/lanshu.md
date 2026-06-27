---
name: lanshu-animated-architecture-diagram
description: Create premium hand-drawn architecture and process diagrams in the Lanshu animated GIF style, with editable .excalidraw files, static PNG previews, and genuinely animated GIFs with moving flow highlights.
tools: Bash, Read, Write
---

# 岚叔动态架构图

Create polished black-background hand-drawn technical diagrams. Follow `SKILL.md` for the full workflow.

## Quick invocation

Read `SKILL.md` for detailed instructions. The core workflow is:

1. Extract diagram content from the user's request
2. Create a spec JSON starting from `assets/default-spec.json`
3. Render with `python3 scripts/render_animated_diagram.py --spec <spec> --outdir <dir> --basename <name> --verify --check`
4. Validate and deliver the three output files (.excalidraw, .png, .gif)

## Key files

- `references/spec-format.md` — spec field reference and copy-length guidance
- `assets/default-spec.json` — template spec to copy and modify
- `scripts/render_animated_diagram.py` — core renderer
