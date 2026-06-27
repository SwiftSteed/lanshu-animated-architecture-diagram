# Lanshu Animated Architecture Diagram

> 岚叔动态架构图: premium hand-drawn animated architecture diagrams for articles, systems, and workflows.

## What this project is

A renderer that turns a structured JSON spec into three outputs:
- `.excalidraw` — editable Excalidraw source
- `.png` — static preview
- `.gif` — genuinely animated diagram with moving glow points and pulsing highlights

## How to use it

This project is registered as a Claude Code skill. When a user asks for 岚叔动态架构图, an architecture diagram in the Lanshu style, an Excalidraw-like diagram, or an animated GIF architecture diagram, invoke it via:

```
/lanshu-animated-architecture-diagram
```

### Direct CLI rendering

If you need to render without going through the skill workflow, call the renderer directly:

```bash
python3 /Users/guopeng/AI-Project/lanshu-animated-architecture-diagram/scripts/render_animated_diagram.py \
  --spec <spec.json> \
  --outdir <output-dir> \
  --basename <name> \
  --verify \
  --check
```

### Available files

| File | Purpose |
|------|---------|
| `SKILL.md` | Primary skill workflow — read this for the step-by-step usage |
| `scripts/render_animated_diagram.py` | Core rendering engine (Python + Pillow) |
| `assets/default-spec.json` | Template spec — start here when creating new diagrams |
| `references/spec-format.md` | Full spec field reference and copy-length guidance |
| `tests/` | Unit tests — run with `python3 -m pytest tests/ -v` |

### Platform compatibility

This project works with **both Claude Code and Codex**:
- Claude Code: invoke via `/lanshu-animated-architecture-diagram`
- Codex: invoke via `$lanshu-animated-architecture-diagram`
- CLI: `python3 scripts/render_animated_diagram.py --spec ...`
- The rendering engine is Python-only; no platform lock-in.
