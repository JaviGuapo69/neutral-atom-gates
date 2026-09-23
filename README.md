# Neutral-Atom Quantum Computing

An interactive page on how a neutral-atom quantum computer works, in five tabs:

1. **What a qubit is** — a short film, with English captions and a chapter list.
2. **Single-qubit gates** — how laser light rotates the Bloch sphere.
3. **Drive one atom** — a live Raman drive on a ⁸⁷Rb qubit. Move a slider and the
   state moves: Ω_eff and the photon-scattering rate are both derived from the same
   beam power, waists and detuning, so a faster gate is always a leakier one.
4. **The CZ gate** — the two-atom Rydberg gate, scrubbable step by step.
5. **Movement extraction** — turning a movie of an atom array back into the
   instruction list that produced it, with a worked example.

**Live at <https://javiguapo69.github.io/neutral-atom-gates/>**

Tabs are linkable: append `#drive`, `#cz` or `#skill` to jump straight in.

## How it works

One HTML file and a media folder. No build step, no framework, no dependencies.

Tabs 3 and 4 are not pictures — they solve the physics in your browser on every
slider move, ported from `bloch_sphere_scattering.py` and `cz_gate_two_atoms.py`.
Tab 4 runs the same RK4 integration over both CZ sectors, {|1⟩,|r⟩} at Ω and
{|11⟩,|W⟩} at √2 Ω, and reports the conditional phase and fidelity it measures
rather than hard-coded numbers.

## Companion repository

The Python tools and the eleven verified SE-cycle transcriptions live in
[neutral-atom-tools](https://github.com/JaviGuapo69/neutral-atom-tools).
