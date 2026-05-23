# FileExplorer

Browse the configured directory.

- **Purpose** — navigate files like a regular file manager, with the entity graph layered on top.
- **Shows** — directory tree, current folder contents, metadata (name, type, size, modified_at), backlink count.
- **Actions** — open `FilePreview`; `open_file_externally`; `move_file`; `delete_file`; navigate folders.
- **States**
  - *tree* — sidebar tree expanded.
  - *list* — flat current-folder list.
  - *empty* — no files in current folder.
- **Composed of** — `BacklinksPanel` for the selected file.
