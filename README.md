# EIP Theorem

**The Epistemic Interface Problem in Multi-Agent Systems**  
*Why Latent-Space Communication Requires a Formal Contract*

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20478868.svg)](https://doi.org/10.5281/zenodo.20478868)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
![EIP Diagram](https://raw.githubusercontent.com/dravitch/eip-theorem/main/image.png)

---

## What this is

This repository contains the formal paper and experimental validation report for the **Epistemic Impossibility Theorem (EIT)**: no communication channel can be simultaneously *gradient-preserving* and *auditable*. These two properties are provably mutually incompatible.

The paper formalises the **Epistemic Interface Problem (EIP)** — the gap between latent-space expressivity (RecursiveMAS, Interlat, KVComm) and formal epistemic accountability (DO-178C, IEC 61508 certified systems) — and proposes the **CLAIM schema** as a minimal formal contract that resolves the EIP under bounded assumptions.

**Status:** Demonstrated and validated (Sprint 0–8) · Working paper v0.2 · ICLR 2027 submission target (August 2026)

---

## Repository structure

```
eip-theorem/
│
├── paper/
│   ├── EIP_paper.tex          # Main paper (LaTeX, English)
│   ├── EIP_paper.pdf          # Compiled — arXiv/Zenodo-ready
│   └── references.bib         # BibTeX bibliography
│
├── report/
│   ├── EIP_validation_report.tex   # Validation report Sprints 0–8 (LaTeX, English)
│   └── EIP_validation_report.pdf   # Compiled
│
├── CITATION.cff               # Standard citation file
├── CHANGELOG.md               # Version history
├── LICENSE                    # CC BY 4.0
└── README.md                  # This file
```

**Experimental validation** (code, CSV results, Sprint records):  
→ [github.com/symbioticode/epistemic-impossibility-validation](https://github.com/symbioticode/epistemic-impossibility-validation)

---

## Key results

| Result | Status |
|--------|--------|
| Gradient Death generalised to all discrete channels | Theorem 3.1 (proven) |
| IB connection scoped to neural softmax implementations | Section 3.3 (corrected v0.2) |
| Expressivity/Accountability boundary: structurally necessary | Theorem 6.1 (proven) |
| CLAIM schema satisfies the EIP | Theorem 5.1 (proven) |
| `belief_mass` + `belnap_state` unified via fuzzy Belnap space | Section 5.5 (new v0.2) |
| Corollary 1 — textual MAS gradient collapse | Confirmed (*p* < 10⁻⁴⁰) |
| Corollary 2 — multi-agent RLHF | Negative result documented |
| Corollary 3 — hybrid architecture circumvents EIT bound | Confirmed (*p* < 0.001) |

---

## How to compile

Requires a standard LaTeX distribution (TeX Live 2023+ or MiKTeX).

```bash
cd paper
pdflatex EIP_paper.tex
bibtex EIP_paper
pdflatex EIP_paper.tex
pdflatex EIP_paper.tex

cd ../report
pdflatex EIP_validation_report.tex
pdflatex EIP_validation_report.tex
```

Or open directly in [Overleaf](https://www.overleaf.com) by uploading the `paper/` folder.

---

## Citation

```bibtex
@misc{dingareassie2026eip,
  author       = {Dinga-Reassi, Andrei},
  title        = {The Epistemic Interface Problem in Multi-Agent Systems:
                  Why Latent-Space Communication Requires a Formal Contract},
  year         = {2026},
  month        = {May},
  version      = {0.2},
  howpublished = {Working paper. Zenodo.},
  doi          = {10.5281/zenodo.XXXXXXX},
  url          = {https://github.com/dravitch/eip-theorem},
  note         = {Developed with the assistance of Claude (Anthropic).
                  Validation: github.com/symbioticode/epistemic-impossibility-validation}
}
```

---

## Intellectual genealogy

This work sits at the intersection of:
- **RecursiveMAS** (Yang et al., 2026) — latent-space MAS communication
- **Information Bottleneck** (Tishby et al., 1999) — information-theoretic communication theory
- **Transferable Belief Model** (Smets, 1994) — formal belief representation
- **Belnap four-valued logic** (Belnap, 1977) — qualified silence and contradiction
- **Fuzzy Belnap space** (Perry & Tsoukias, 1998) — continuous epistemic states

---

## Related work by the same author

- **D-SIG Standard** — Distilled Signal Standard for IT observability  
  [github.com/dravitch/dsig-standard](https://github.com/dravitch/dsig-standard) · Zenodo: [10.5281/zenodo.19186972](https://doi.org/10.5281/zenodo.19186972)

---

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to share and adapt this material for any purpose, provided appropriate credit is given.

---

*Working paper v0.2 · May 2026 · Andrei Dinga-Reassi*
