---
title: Significant Prover9 Result
description: Commutative AIM proven nilpotent of class 3 with advanced Prover9 methods
theme: minima
---

# Significant Prover9 Result

**October 7, 2025 — Albuquerque, NM**  
**[AI4REASON co-founder Bob Veroff](https://www.cs.unm.edu/~veroff/)** has announced an important result in automated reasoning:  
Prover9 has produced a **complete proof that the commutative AIM theory (AIM + x * y = y * x) is nilpotent of class 3**.

While the result is not new mathematically — given the previously established proof of nilpotency class 3 for AIM by **Michael Kinyon** and **Petr Vojtěchovský** — it represents a **significant achievement in automated reasoning**.  
This result is among the most complex ever produced by Prover9, demonstrating the power of large-scale iterative reasoning guided by hint-based methods.

---- 

## Overview

The latest result is a proof that AIM + Commutativity implies clause **nil3 24 (a(a(a(x,y,z),u,w),v5,v6) = 1)**,
which suffices to prove nilpotency class 3 because of previous Prover9 results. 

The result was proved by multiple coordinated Prover9 runs.

 - **Proof duration:** 40 days
 - **Proof established:** *September 16, 2025*

The proof was then extracted from the multiple output files and confirmed with a single Prover9 run for posting.

- **Total proof length:** 30,835 clauses
- **Level:** 314
- **Maximum clause weight:** 78
- **Given clauses in proof:** 8,940

## The Method

This discovery was achieved using the Bigloop method. A Bigloop
run consists of a number of P9loop runs running simultaneously, typically
with different Prover9 search settings. Each P9loop run consists of
a sequence of Prover9 runs, typically using different term orderings.
Each new invocation of Prover9 includes as input lemmas all hint matchers
from all of the completed Prover9 runs from all of the P9loop sequences.

The key proof relied on one Bigloop run consisting of 3 P9loop processes,
each set up to iterate over 36 term orderings. The Prover9 runs all
relied on the same set of input hints coming from previous Prover9 AIM
proofs. This proof was established in 61 output files with a network
of clause derivation dependencies between the files.

The proof posted on the <a href="www.cs.unm.edu/~veroff/AIM_REDONE">AIM
project page</a> is the result of extracting a single proof from the
Bigloop files and eliminating several lemmas that we typically use
when searching for new results.

---

## Development Timeline

### September 16, 2025 — Proof Found  
Bigloop found a proof of nil3 30, which was then confirmed with Prover9
to prove nil3 24, completing a proof that AIM + Commutativity implies
nilpotency class 3.

The Bigloop run spanned  **40 days**, from *August 7, 2025* to *September 16, 2025* and generated 61 Prover9 output files.

### October 6, 2025 — Complete Proof 
Reconstructing the full derivation across 61 files required multiple reruns with enhanced logging to expose hidden clause dependencies.  
All derivations were successfully extracted, giving a complete proof, though still distributed across several runs.

### October 8, 2025 — Unified Run  
A single-run proof was achieved, confirming the result in one continuous Prover9 execution.

### October 17, 2025 — Final Verification  
Veroff confirmed a final proof **based solely on the AIM axioms and Commutativity**, without auxiliary lemmas often used in related derivations.

---

## Significance

This work demonstrates the capabilities of modern automated reasoning systems to tackle **very deep and interconnected search spaces**.  
The result showcases methodological advances such as:  
- Coordinated multi-run reasoning (*Bigloop* / *P9loop*)  
- Iterative lemma extraction and hint propagation  
- Long-duration autonomous search with proof reconstruction  

Such techniques highlight how reasoning engines like **Prover9** can continue to make progress on longstanding algebraic problems through algorithmic innovation and persistence.

---

Further information and background materials are available on the [AIM project page](https://www.cs.unm.edu/~veroff/AIM_REDONE/).

---

© AI4REASON Institute 2025  

Business ID (IČ): 23753161
