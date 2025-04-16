# At The Edge Of Chaos

This Pure Data (Pd) abstraction is part of the artistic research project **"At the Edge of Chaos"**, developed during the **Ligeti Zentrum's Scientists & Artists in Residence Program 2025** by **Moises Horta Valenzuela**.

The project proposes a novel integration of the **Impulse Pattern Formation (IPF)** algorithm with **RAVE (Realtime Audio Variational autoEncoder)** neural networks to generate dynamic, multi-channel audio performances. Rooted in the mathematical framework of IPF—described in Linke et al. (2019) as a recursive system of impulse reflection and feedback—the model exhibits complex behaviors such as stability, bifurcation, and chaos.

By mapping IPF's emergent behavior to the **latent space** of RAVE models, this system enables the real-time control of multiple parallel RAVE instances, each acting as a distinct virtual instrument or sonic character. This creates coordinated spatial audio events that combine deterministic structure with unpredictable complexity.

This repository contains Pure Data patches developed during the residency that demonstrate the interaction between IPF and RAVE, and serves as a toolkit for further research and creative development.

---

## Project Background

This research explores the question of integrating complex systems, specifically the **Impulse Pattern Formulation (IPF)** model with **RAVE (Realtime Audio Variational autoEncoder)** neural synthesis. 

Based on the mathematical formulation of IPF as presented in Linke et al. (2019), this project leverages the model's ability to generate complex temporal dynamics—ranging from stability to chaos—through recursive feedback and delayed impulse interaction. These dynamics correspond to identifiable **behavioral regions** within the system, including:

- **Stable Region**: Where the system produces predictable, periodic output patterns
- **Chaotic Region**: Where the output becomes unpredictable and highly sensitive to small changes in input
- **Edge-of-Chaos Region**: A transitional zone where the system exhibits a balance between order and unpredictability, ideal for dynamic sonic control

The primary goal is to harness these regions to control the **latent space** of RAVE, resulting in expressive neural audio synthesis that blends deterministic modulation with emergent behavior.

---

## Requirements

To run this project, you will need the following Pure Data setup:

- **Pure Data 0.55** or later  
- The **nn~ external** for neural synthesis ([GitHub repo](https://github.com/acids-ircam/nn_tilde))  
- The **ELSE** library, installable via **Dekken** inside Pure Data  
- A trained RAVE model file, such as `percussion.ts`, downloadable from:  
  https://play.forum.ircam.fr/rave-vst-api/get_model/percussion

---

## Repository Contents

- `ipf.pd` – Core IPF abstraction  
- `rave-ipf-example.pd` – Example patch showing IPF modulation of RAVE  
- `README.md` – This file  

---

## Usage Instructions

1. Open the `rave-ipf-example.pd` patch.
2. Ensure that `nn~` is properly installed and that you have a trained RAVE model available.
3. Use the GUI to adjust IPF parameters such as **Frequency**, **Alpha**, and **Beta**.
4. Observe how the system’s behavior shifts across stability, chaos, and edge-of-chaos zones in real time.
5. Use toggle switches to explore first- and second-order IPF models or force transitions between stable and chaotic modes.
6. The resulting modulation will dynamically control the latent parameters of one or more RAVE instances, producing highly varied and responsive audio outputs.

---

## Reference

Linke, S., Bader, R., & Mores, R. (2019). *The Impulse Pattern Formulation (IPF) as a Model of Musical Instruments – Investigation of Stability and Limits*. Chaos: An Interdisciplinary Journal of Nonlinear Science.  
DOI: [10.1063/1.5092511](https://doi.org/10.1063/1.5092511)

---

## Credits

Developed by **Moisés Horta Valenzuela**  
**Ligeti Zentrum, Scientists & Artists in Residence Program 2025**

---

## License

MIT License. You are free to use, modify, and distribute this code with proper attribution.
