# At The Edge Of Chaos

This Pure Data (Pd) abstraction is part of the research project **"At the Edge of Chaos"**, developed during the **Ligeti Zentrum's Scientists & Artists in Residence Program 2025**. The author of the code is **Moisés Horta Valenzuela**.

---

## Project Background

This research explores the question of integrating complex systems, specifically the **Impulse Pattern Formulation (IPF)** model with **RAVE (Realtime Audio Variational autoEncoder)** neural synthesis. 

Based on the mathematical formulation of IPF as presented in Linke et al. (2019), this project leverages the model's ability to generate complex temporal dynamics—ranging from stability to chaos—through recursive feedback and delayed impulse interaction. These dynamics correspond to identifiable **behavioral regions** within the system, including:

- **Stable Region**: Where the system produces predictable, periodic output patterns
- **Chaotic Region**: Where the output becomes unpredictable and highly sensitive to small changes in input
- **Edge-of-Chaos Region**: A transitional zone where the system exhibits a balance between order and unpredictability, ideal for dynamic sonic control

The primary goal is to harness these regions to control the **latent space** of RAVE, resulting in expressive, multi-channel audio synthesis that blends deterministic modulation with emergent behavior.

Each RAVE instance functions as a unique virtual voice or instrument. The system is designed around three central strategies:

- **Parameter-space mapping**: Linking IPF’s parameters (alpha α, beta β, etc.) to RAVE's latent coordinates for expressive modulation
- **Topology-aware coupling**: Using IPF’s delay/reflection topology to influence multiple RAVE instances in parallel
- **Multi-scale integration**: Managing sonic structure at both the microsound and formal compositional levels

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
