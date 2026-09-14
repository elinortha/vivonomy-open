# Vivonomy open data

Vivonomy is a map of how biomass feedstocks such as sawdust, corn stalks, manure, algae and food waste can be turned into products such as fuels, chemicals, soil amendments and heat. The map is a graph you can walk from any feedstock to any product, and it has a waist: many feedstocks converge on a few platform intermediates (sugars, syngas, bio-oil, biogas) and then diverge into many products. This repository holds that graph and the data behind it, in the same form the site at [vivonomy.bio](https://vivonomy.bio) shows.

Values come from source-tied claim records that a reviewer has checked; only checked records count toward a published value.

## What is here

| Path | What it is |
|---|---|
| `data/graph.json` | the graph with its records: every node and edge, and for each measured property the list of records with value, unit, source and review status |
| `data/aggregates.json` | for each node and property, the published value, its evidence grade, and whether it rests on records a reviewer has checked |
| `data/pathways.json` | routes composed across several steps, with a figure for the whole route |
| `data/sources.json` | the sources the data draws on, each with a label, a year and whether it has been read yet |
| `data/nodes/<layer>/*.yaml` | the nodes of the graph, one file each, by layer: feedstock, pretreatment, primary_conversion, platform, upgrading, product |
| `data/edges/*.yaml` | the edges of the graph, one file each, named `source__target` |
| `data/pathways/*.yaml` | the declared routes that `pathways.json` is composed from |
| `data/sources/bibliography.yaml` | every source the records cite: identifier, citation label, year and kind |
| `data/sources/papers.yaml` | the papers in the reading list whose licence allows redistribution: DOI, title, year and licence |
| `papers/` | the full texts of those papers that are held here, with their authors' attribution intact |
| `data/MANIFEST.json` | the date of this publish, the revision it was made from, and the size and SHA-256 of every file |

## How to cite

Vivonomy (2026). Vivonomy open bioeconomy pathway data, published 2026-09-14. https://vivonomy.bio

## Licence

The data in this repository is released under the Creative Commons Attribution 4.0 International licence (CC-BY 4.0); the full text is in `LICENSE`. The papers in `papers/` are the work of their authors, released by them under CC-BY 4.0, and keep their own attribution. The Vivonomy name and marks are not covered by this licence.
