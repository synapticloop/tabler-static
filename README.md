# Tabler Static Build

This repository provides an automated, pre-compiled static distribution of the **Tabler** dashboard UI kit.

## Project Purpose

The goal of this repository is to provide a pre-compiled, "plug-and-play" version of Tabler's static assets. This allows for quick deployment or integration without requiring a full Node.js build environment.

## ⚠️ Support the Original Project

This repository is an automated mirror and build distribution. All credit for the design and development of these assets goes to the Tabler team. If you find these assets useful, please support the original creators by starring their repo or contributing to their project.

**Original Repository:** [https://github.com/tabler/tabler/](https://github.com/tabler/tabler/)

---

## Project Overview

This project is designed for developers who want to use Tabler's static assets (CSS, JS, and HTML) without maintaining a local Node.js/pnpm build environment.

* **Automated Sync:** This repository checks the source Tabler repository for updates every hour.
* **Plug-and-Play:** All compiled assets are located in the `/static/` directory.
* **Downloadable Bundles:** Pre-packaged `.zip` files of the latest build are available in the root directory.

## How the Automation Works

The build process is managed by a custom Bash script running via a cron job on a Linux instance.

1.  **Check:** The script pulls the latest code from the official Tabler repository.
2.  **Build:** If new changes are detected, it performs a clean build using `pnpm`.
3.  **Sync:** It fetches the latest version of this `README.md` from GitHub to preserve any manual edits.
4.  **Deploy:** It cleans the old assets, copies the new build into the `/static/` folder, and pushes the changes back to this repo.

If the source repository has not changed, the script exits without performing a build to save resources.

## License

Both this distribution and the underlying Tabler framework are licensed under the **MIT License**.

---

## Documentation

For detailed information on how to use Tabler components and layouts, please see:
* [tabler-README.md](./tabler-README.md) — The original documentation from the source.
* [Official Tabler Docs](https://tabler.io/docs) — Comprehensive online guide.


*Last automated build: {{LAST_BUILD_DATE}}*
