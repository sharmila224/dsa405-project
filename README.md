# DSA 405 Project: Hard Drive Reliability

## What this project is
This project studies whether certain hard drive manufacturers and models fail
earlier under real datacenter workloads, and whether a drive's self-reported
health readings (SMART attributes) rise before a failure. The goal is to help
anyone running storage at scale decide what to buy and when to replace it.

## Where the data came from
- **Backblaze Drive Stats** (primary source). Daily snapshots of every drive in
  Backblaze's datacenters, published openly by Backblaze, Inc. since 2013.
  https://www.backblaze.com/cloud-storage/resources/hard-drive-test-data
  The file in `data/raw/` is one daily snapshot (2026-01-01) from Q1 2026,
  reduced to the columns this project uses and gzip-compressed. See
  `data/raw/SOURCES.md` for the exact download date and columns.
- **Wikipedia drive specification tables** (second source, added in P3) will
  provide per-model specifications to join on the drive model.

The raw data in `data/raw/` is preserved unmodified. The notebook reads it over
the web and never writes to that folder.

## How to run it
1. Open `DSA405_002_FA26_P2_sshirol.ipynb` in Google Colab (use the Colab
   button at the top of the notebook on GitHub).
2. Runtime > Restart session and run all.
3. The notebook reads the data directly from this repository, so there is
   nothing to download first.

## Repository layout
- `data/raw/` — raw data file and SOURCES.md (not modified by any code)
- `DSA405_002_FA26_P2_sshirol.ipynb` — audit, cleaning log, and provenance brief
