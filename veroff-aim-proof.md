---
title: Significant Prover9 Result
description: Commutative AIM proven nilpotent of class 3 with advanced Prover9 methods
theme: minima
---

# Significant Prover9 Result

**October 7 2025 — Albuquerque, NM**  
**[AI4REASON co-founder Bob Veroff](https://www.cs.unm.edu/~veroff/)** has announced an important result in automated reasoning:  
Prover9 has produced a **complete proof that the commutative AIM theory (AIM + x * y = y * x) is nilpotent of class 3**.

While the result is not new mathematically — given the previously established proof of nilpotency class 3 for AIM by **Michael Kinyon** and **Petr Vojtěchovský** — it represents a **significant achievement in automated reasoning**.  
This proof is among the most complex ever produced by Prover9, demonstrating the power of large-scale iterative reasoning guided by hint-based methods.

---

## Overview

- **Proof duration:** 40 days  
- **Proof found:** *September 16 2025*  
- **Total proof length:** 30 835 clauses (14 626 new hints)  
- **Level:** 314  
- **Maximum clause weight:** 1033 (78 w/o degradation)  
- **Given clauses in proof:** 8 940  

The discovery was achieved using the **Bigloop** method — a sophisticated multi-run Prover9 strategy that coordinates several iterative search loops (*P9loop*), each exploring different term orderings and exchanging hint matchers between runs.  

One Bigloop run consisting of three P9loop processes (iterating across 36 term orderings) produced a network of 61 output files, culminating in the derivation of the empty clause in `P9loop_1.22`.

---

## Development Timeline

### September 16 2025 — Proof Found  
Prover9 completed the proof of **nil3 24**, establishing that AIM + Commutativity implies nilpotency class 3.

### October 1 2025 — Extraction  
Reconstructing the full derivation across 61 files required multiple reruns with enhanced logging to expose hidden clause dependencies.  
The total Bigloop computation spanned **40 days**, from *August 7 2025* to *September 16 2025*.

### October 6 2025 — Complete Proof  
All derivations were successfully extracted, giving a complete proof, though still distributed across several runs.

### October 8 2025 — Unified Run  
A single-run proof was achieved, confirming the result in one continuous Prover9 execution.

### October 17 2025 — Final Verification  
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

Further information and background materials are available on  
[Bob Veroff’s AIM Redone page](https://www.cs.unm.edu/~veroff/AIM_REDONE/).

---

© AI4REASON Institute 2025  

Business ID (IČ): 23753161