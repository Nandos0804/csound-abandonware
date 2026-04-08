# Contributing to Csound Abandonware Archive

Thank you for helping preserve Csound's software heritage! This repository uses **Git LFS** to store archived binary files (`.tar.gz`, `.zip`, `.tgz`, etc.).

## Prerequisites

- [Git LFS](https://git-lfs.github.com/) installed and initialized (`git lfs install`)

## How to Contribute

1. **Fork** this repository.
2. **Create a branch** named after the software you are archiving:

   ```bash
   git checkout -b software-name
   ```

   For example: `cecilia5`, `cmask`, `winsound`.

3. **Place the archive file(s)** in the correct folder:
   - `Linux/` — Linux **binaries**
   - `Mac/` — macOS **binaries**
   - `Windows/` — Windows **binaries**
   - `src/` — source code archives and cross-platform source tarballs
   - `Unsorted/` — files you are unsure about

   **Rule of thumb:** platform-specific binaries go in `Linux/`, `Mac/`, or `Windows/`. Source code and source tarballs go in `src/`. If unsure, use `Unsorted/`.

4. **Update `README.md`** — add or complete the entry for the software:
   - Name and version
   - Original description (copy from the project's original page)
   - Author(s)
   - Original URL or archive link (Wayback Machine, SourceForge, GitHub, etc.)
   - Screenshot (if available, place it in a `screenshots/` folder)
5. **Commit and push** your branch using the conventional commit format `software(type): description`:

   ```bash
   git add .
   git commit -m "cecilia(feat): add v2.0.5 archive"
   git push origin software-name
   ```

   Common types: `feat` (new archive/entry), `fix` (corrections), `chore` (maintenance), `docs` (documentation only).

   More examples:
   - `cmask(feat): add macOS binary`
   - `cecilia(chore): correct documentation`
   - `winsound(docs): add original description`

6. **Open a Pull Request** against `main`.

## Guidelines

- **One software per branch / PR** — keeps reviews focused.
- **Do not modify or repackage** the original archives. We want bit-for-bit preservation.
- **Provide provenance** — always note where you obtained the file (direct download link, Wayback Machine URL, personal archive, etc.).
- **Respect licenses** — only upload software that was publicly distributed. Note the original license in the README entry.
- **Large files** are handled automatically by Git LFS via `.gitattributes`. No extra steps needed beyond having LFS installed.

## README Entry Template

```markdown
### Software Name vX.Y.Z

|                        |                                                               |
| ---------------------- | ------------------------------------------------------------- |
| **Author(s)**          | First Last                                                    |
| **License**            | GPLv2 / LGPL / etc.                                           |
| **Platform**           | Linux / Mac / Windows / Cross-platform                        |
| **Original URL**       | [example.com](https://example.com)                            |
| **Archive URL**        | [Wayback Machine](https://web.archive.org/web/...)            |
| **Archive file**       | `filename.tar.gz`                                             |
| **Paper**              | [Paper title](https://example.com/paper.pdf) _(if available)_ |
| **Last compatible OS** | Windows XP / macOS 10.6 / etc. _(if known)_                   |

> Original description copied verbatim from the project page.

<!-- optional screenshot -->

![Screenshot](screenshots/software-name.png)
```

## Contact

If you believe a software entry is missing, needs to be added, or should be removed from this archive, please reach out at **<giuseppeernandez@hotmail.it>**.
