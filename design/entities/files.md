# Files

A configured directory on disk, surfaced inside the app as a tree and a viewer. The files are just regular files — they live in the filesystem, not in the entity graph.

## What you get

- **Tree** — the directory in the sidebar, expand / collapse, mirrors the filesystem as-is
- **Viewer** — inline preview for the common types: PDFs, images, audio, video, text, code, markdown
- **Search** — full-text search across file contents, alongside the rest of your workspace
- **Open externally** — hand off to the native app for anything the viewer doesn't render

## The agent and files

The [agent](../agent/overview.md) can read, edit, create, move, and delete files in the directory. File operations are shown like any other action — visible, confirmable, reversible. Files are just one more surface the agent can work on.

## What it is not

- Not an entity in the graph — files have no links or backlinks; they're just files
- Not a storage layer — the app doesn't copy, own, or sync; what's on disk is what you see
- Not connected — if you want structural links between pieces of writing, use a [document](documents.md), not a file

## What lives elsewhere

- Long-form writing with links and backlinks → [documents](documents.md)
- Meeting recordings — drop them in the directory; reference the filename in the [meeting](meetings.md) note if you want
