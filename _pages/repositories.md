---
layout: page
permalink: /tools/
title: Tools
description: I spend most of my time tinkering with program analysis tools.
nav: true
nav_order: 4
---


* [Crab](https://github.com/LinerSu/crab/tree/sas_2026): An abstract interpretation library for LLVM, contributed 4 novel domains for memory-access validation, object invariant inference, and heap-aware taint analysis
    * Most-Recently-Used Abstract Domain ([MRUD](https://github.com/LinerSu/crab/blob/sas_2026/include/crab/domains/object_domain.hpp)): a memory domain for reason object invariants, with novel support for avoiding weak updates.
    * Symbolic Equality Abstract Domain ([VarEq](https://github.com/LinerSu/crab/blob/sas_2026/include/crab/domains/symbolic_variable_eq_domain.hpp)): an equality domain using union-find data structure to track equivalence classes of symbolic variables.
    * Template-Difference-Bound-Matrix Abstract Domain ([TemplateDBM](https://github.com/LinerSu/crab/blob/sas_2026/include/crab/domains/tvpi_split_dbm.hpp)): a coeffeicient template domain for linear inequalities, especially for two-variable-per-inequality (TVPI) constraints.
    * Data-flow Tag Analysis over Recency Abstract Domain ([DFA](https://github.com/LinerSu/crab/blob/sas_2026/include/crab/domains/region_domain.hpp)): a dataflow analysis for tracking tainted tags over heap objects, with domain reduction over memory domain.
* [SeaDSA](https://github.com/LinerSu/sea-dsa/tree/dsa-chunk): A points-to analysis for LLVM with interval-aware extensions for finer-grained object disjointness and pointer alias disambiguation
* [SeaBMC](https://github.com/seahorn/seahorn/tree/dev14): A bounded model checker for LLVM; integrates Crab pre-analysis passes to prune provable assertions and speed up BMC encoding and SMT solving
* [Drift](https://github.com/nyu-acsys/drift): An abstract-interpretation-based data flow refinement type inference tool — POPL 2021