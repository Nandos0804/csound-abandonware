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
3. **Place the archive file(s)** in the correct platform folder:
   - `Linux/` — Linux builds and source tarballs
   - `Mac/` — macOS builds
   - `Windows/` — Windows builds
   - If you are unsure about the correct folder, use Unsorted.
4. **Update `README.md`** — add or complete the entry for the software:
   - Name and version
   - Original description (copy from the project's original page)
   - Author(s)
   - Original URL or archive link (Wayback Machine, SourceForge, GitHub, etc.)
   - Screenshot (if available, place it in a `screenshots/` folder)
5. **Commit and push** your branch:

   ```bash
   git add .
   git commit -m "Add <software-name> v<version>"
   git push origin software-name
   ```

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

|                  |                                                    |
| ---------------- | -------------------------------------------------- |
| **Author(s)**    | First Last                                         |
| **License**      | GPLv2 / LGPL / etc.                                |
| **Platform**     | Linux / Mac / Windows / Cross-platform             |
| **Original URL** | [example.com](https://example.com)                 |
| **Archive URL**  | [Wayback Machine](https://web.archive.org/web/...) |
| **Archive file** | `filename.tar.gz`                                  |

> Original description copied verbatim from the project page.

<!-- optional screenshot -->

![Screenshot](screenshots/software-name.png)
```
