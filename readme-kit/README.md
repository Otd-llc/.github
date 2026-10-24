# readme-kit

The shared header and footer for every OTD repo README. The `otd-readme` skill in Otd-llc/otd-skills owns the rules. This folder holds the exact text so no repo has to retype it from memory.

**Status** · active · **Version** · footer v1, 2026-10-23

## Use it

1. Copy [`header.md`](header.md) to the top of the README and fill it in. If the repo has no committed hero yet, delete the two `<p align="center">` blocks and start at the H1. Never leave a placeholder image.
2. Copy [`footer.md`](footer.md) to the bottom, unchanged, including its version comment.
3. Edit the `## License` line only when the repo has a `LICENSE` file. Then name its holder exactly as written there, link it, and give the SPDX id if the repo is open.
4. Run `node skills/otd-readme/scripts/readme_check.mjs <repo>` from otd-skills. It should report zero FAIL.

## Rules

- **The footer is identical in every repo.** Change it here first, bump the version comment (`footer v2`), then roll it out. A sweep finds outdated footers by that comment.
- **Header links come from one vocabulary, in this order:** `Live`, `Demo`, `Docs`, `Assets`, `Changelog`, `Status`. Skip any that don't exist.
- **Status is one word:** `active`, `experimental`, `frozen` or `archived`.
- **Images:** one dark-baked asset in the repo's own `.github/assets/`, copied in, never hotlinked from here. No `<picture>`, no `#gh-*-mode-only`.
- **No shared mark image yet.** Any image added to this kit gets an owner sandbox round first.
