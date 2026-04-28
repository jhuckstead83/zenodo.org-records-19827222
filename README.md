# Phase-Locked Extreme Compression in Adjacent Zeta-Zero Spacing

This repository accompanies the preprint:

**Phase-Locked Extreme Compression in Adjacent Zeta-Zero Spacing: A Seam-Stitched Empirical Study Through the Full Available LMFDB Horizon**

Frozen paper record on Zenodo: [https://zenodo.org/records/19827222](https://zenodo.org/records/19827222)

## Overview

This project studies rare extreme compressions in adjacent spacing between consecutive nontrivial zeros of the Riemann zeta function on the critical line.

The analysis is built on a **seam-stitched observational board** constructed from the available LMFDB horizon with explicit carry-state preservation across shard boundaries. Adjacent-zero gaps that cross file seams are preserved rather than discarded. On this board, local spacing summaries are compared to a fitted local spacing spine, a row-level compression score is defined, and connected packets of the most extreme compressions are extracted under frozen morphology rules.

The main empirical finding is that these packets are not phase-neutral. Across broad-board resolution ablations at **130k, 90k, 70k, and 52k zeros per row**, the dominant organizing coordinate remains the first logarithmic harmonic

`h1(T) = frac(log(T / 2π) / π)`

and the trimmed late-stage continuation audit consistently selects **quadratic** models for both the local drift coefficient `b1` and the local curvature coefficient `b2`.

A direct terminal-band comparator on the final **28.5B to 31.5B** segment strengthens this picture. The unusually tight `h1` locking persists at **52k, 8k, and 1k** resolution, with the **8k** board yielding the strongest concentration of the three. Additional reinforcement comes from:

- a terminal **8k matched-packet placement null** over **2048** replicates
- a terminal **8k threshold-stability sweep**
- a **10,000-run jackknife robustness audit**

## What this repository contains

This repository is intended to be a **reproducibility front door**, not a full archival dump of every large intermediate dataset.

It contains:

- paper source and compiled manuscript
- lightweight analysis code and notebooks
- summary artifacts supporting the main reported results
- release notes and artifact maps for traceability

Large decoded stores and heavy intermediate parquets are archived separately and are not the primary focus of the repository.

## Core evidence stack

The current revision rests on four main layers:

1. **Broad-board resolution ablation**  
   The dominant harmonic remains `h1` across 130k, 90k, 70k, and 52k boards.

2. **Terminal-band ladder**  
   The final 28.5B to 31.5B segment is compared directly at 52k, 8k, and 1k resolution.

3. **Matched-packet null**  
   On the terminal 8k board, the real field exceeds all 2048 matched-packet null replicates.

4. **Jackknife robustness**  
   On the same terminal 8k field, the `h1` lock remains highly stable after repeated random removal of 20% of packets.

## Main claim

The main claim is intentionally **empirical and observed-horizon in scope**:

- rare extreme compressions organize reproducibly in the first logarithmic harmonic
- this organization is stable under substantial row-size ablation
- the terminal band exhibits unusually tight local `h1` locking
- the observed terminal concentration is not explained by packet morphology alone or by a small outlier subset

## What is not claimed

This repository does **not** claim:

- a closed asymptotic law beyond the observed horizon
- a proof of the Riemann Hypothesis
- that the fitted continuation family is a theorem at arbitrarily greater heights

The results are presented as a frozen observed-horizon empirical law supported by seam diagnostics, resolution ablation, terminal comparators, null testing, threshold replay, and packet-level robustness audits.

## Repository layout

A typical structure for this repository is:

```text
paper/        manuscript source and compiled PDF
src/          lightweight reusable analysis code
notebooks/    notebooks reproducing headline tables and figures
artifacts/    summary CSV/JSON outputs, manifests, release notes
docs/         method overview, artifact map, changelog
```
## Suggested reading path

For a quick audit, start with:

1. the manuscript in paper/
2. the terminal comparator summaries
3. the terminal 8k null summary
4 the terminal 8k jackknife summary

## Citation

Please cite the Zenodo record for the frozen paper version:

https://zenodo.org/records/19827222

Author

Jeffery Huckstead,
Independent Researcher
