# At-The-Edge-Of-Chaos

This Pure Data (Pd) abstraction is part of the research project **"At the Edge of Chaos"**, developed during the **Ligeti Zentrum's Scientists & Artists in Residence Program 2025**. The author of the code is **Moisés Horta Valenzuela**.

---

## Project Background

This research explores the question of integrating complex systems, specifically the **Impulse Pattern Formulation (IPF)** model with **RAVE (Realtime Audio Variational autoEncoder)** neural synthesis. 
Based on the mathematical formulation of IPF as presented in Linke et al. (2019), this project leverages the model's ability to generate complex temporal dynamics—ranging from stable to chaotic behavior—through recursive feedback and delayed impulse interaction.

The main objective is to use IPF’s behavior to control the **latent space** of RAVE, a neural audio synthesizer, allowing for expressive, multi-channel audio synthesis that blends deterministic control with emergent complexity.

Each RAVE model acts as a virtual instrument or voice, modulated in real time by IPF’s output. The system is designed around three core principles:

- **Parameter-space mapping**: Connecting IPF’s alpha (α) and beta (β) parameters to RAVE’s latent space coordinates.
- **Topology-aware coupling**: Reflecting IPF’s internal feedback and delay network structure across multiple RAVE instances.
- **Multi-scale integration**: Managing sound at both the micro (sample/synthesis) and macro (structure/form) levels.

---

## Requirements

To run this project, you will need the following Pure Data setup:

- **Pure Data 0.55** or later  
- The **nn~ external** for neural synthesis (https://github.com/acids-ircam/nn_tilde)  
- The **ELSE** library, installable via **Dekken** inside Pure Data  

---

## Repository Contents

- `ipf.pd` – Core IPF abstraction  
- `rave-ipf-example.pd` – Example patch showing IPF modulation of RAVE
-  `percussion.ts` – Example pre-trained RAVE model
- `README.md` – This file  

---

## Usage Instructions

1. Open the `rave-ipf-example.pd` patch.
2. Make sure `nn~` is properly installed and linked to a trained RAVE model.
3. Adjust parameters such as Frequency, Alpha, and Beta using the GUI.
4. Monitor how the system dynamically controls the latent space of one or more RAVE instances.
5. Use the toggle controls to switch between stable and chaotic behaviors, or between first- and second-order IPF models.

---

## Reference

Linke, S., Bader, R., & Mores, R. (2019). *The Impulse Pattern Formulation (IPF) as a Model of Musical Instruments – Investigation of Stability and Limits*. Chaos: An Interdisciplinary Journal of Nonlinear Science. DOI: [10.1063/1.5092511](https://doi.org/10.1063/1.5092511)

---

## Credits

Developed by **Moisés Horta Valenzuela**  
Ligeti Zentrum, Scientists & Artists in Residence Program 2025

---

## License

MIT License. You are free to use, modify, and distribute this code with proper attribution.

