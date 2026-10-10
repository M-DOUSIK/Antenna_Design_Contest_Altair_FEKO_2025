# Elliptical Reflector Antenna for Microwave Tumour Therapy

A 2.45 GHz microstrip patch antenna paired with an elliptical reflector that focuses microwave energy onto a target region. Designed and simulated in Altair Feko.

![Altair Feko](https://img.shields.io/badge/Altair_Feko-2024-005A9C)
![Frequency](https://img.shields.io/badge/ISM_band-2.45_GHz-informational)
![Award](https://img.shields.io/badge/🏆_1st_Place-Altair_×_Siemens_Student_Competition-gold)
![License](https://img.shields.io/badge/license-CC_BY_4.0-green)

> 🏆 **First place, Altair × Siemens Student Competition 2025 (with AICTE), with a ₹10,000 cash prize.** See the [announcement on LinkedIn](https://www.linkedin.com/posts/dousikmanokaran_teamsiemens-siemens-aicte-activity-7311790777838313473-6UL7).
>
> ▶️ **[Watch the video walkthrough](https://www.youtube.com/watch?v=hx8wSjsUkmU)**

---

## Overview

The project studies how a focused ISM-band source can be used for two tumour-treatment mechanisms:

- **Microwave ablation.** Concentrated energy heats and destroys tumour tissue.
- **Polarisation-based disruption.** Circularly polarised fields are used to interfere with cell division.

An elliptical reflector has two focal points. With the patch antenna at the first focus, the reflected wavefront converges on the second, so energy is delivered to a small region instead of spreading through the surrounding tissue.

## Design

| Stage | What was done |
|---|---|
| Frequency selection | 2.45 GHz ISM band, a trade-off between tissue penetration and focal spot size |
| Antenna | Broadband microstrip patch antenna, 50 Ω port, tuned for the selected band |
| Reflector | Elliptical reflector with the feed at focal point F1 and the target at F2 |
| Analysis | VSWR / impedance match at the port, Specific Absorption Rate (SAR), and field concentration at F2 |

## Repository Structure

```
.
├── simulation/            Altair Feko project
│   ├── AntSim.cfx         CADFEKO model (open this)
│   ├── AntSim.pre         PREFEKO input
│   ├── AntSim.fek         Solver input
│   ├── AntSim.out         Solver output log
│   ├── AntSim.bof         Binary results (for POSTFEKO)
│   ├── AntSim.pfs         POSTFEKO session
│   └── AntSim.afo, .cfm   Auxiliary model / mesh data
└── docs/
    └── presentation.pptx  Contest presentation
```

## Running the Simulation

1. Install **Altair Feko 2024** or later. The project was solved with Feko 2024 (build 2024-4313).
2. Clone the repository:
   ```sh
   git clone https://github.com/M-DOUSIK/Antenna_Design_Contest_Altair_FEKO_2025.git
   ```
3. Open `simulation/AntSim.cfx` in **CADFEKO** to inspect or edit the geometry.
4. Run the solver. To view the results without re-solving, open `simulation/AntSim.pfs` in **POSTFEKO**.
5. Sweep the frequency or the reflector dimensions to explore the focusing behaviour.

## Future Work

- Fabricate a physical prototype and measure S11 and the radiation pattern.
- Replace the simple target with layered, frequency-dependent tissue models.
- Study clinical feasibility, including thermal modelling and safe exposure limits.

## License

The simulation models, results and presentation are licensed under [CC BY 4.0](LICENSE). You may reuse and adapt them with attribution.

## Contact

**Dousik Manokaran**: [m.dousik@gmail.com](mailto:m.dousik@gmail.com) · [LinkedIn](https://www.linkedin.com/in/dousikmanokaran/)
