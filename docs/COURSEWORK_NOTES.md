# Translated coursework context

The source is Homework 7, “W2_3: Continuous Attractor Neural Network”, from a Neural Computation Modelling Workshop.

## Objectives

Understand the recurrent activity equation and divisive rate normalisation, periodic Gaussian connectivity, one- and two-dimensional feature spaces, CANNs tracking tasks and activity visualisation. Implement model state, wrapped distance, connectivity, stimulus generation and Euler updates. Optional work explores parameters, noisy inputs, multiple bumps and possible biological modelling interpretations.

## Core assignment

Run the built-in CANN1D and CANN2D models on smooth tracking tasks, then implement custom counterparts and repeat the tasks. The source includes filled-in learner implementations and separate complete answer keys.

Both learner connectivity formulas place a Gaussian scaling factor inside the exponent; the provided reference answers place it outside. The prepared classes use the reference formulas and document the correction. This does not claim independent completion of the reference material.

The main 2D experiment has six waypoints and five intervals totalling 60 model-time units. The reference-answer path has five waypoints and four intervals totalling 40. The prepared comparison consistently uses the main path. Likewise four 1D control positions imply three intervals, not four, and its two moving segments have equal speeds.

## Optional noisy-template exercise

Use a 128-neuron custom model and TemplateMatching1D at position zero for duration 50. Compare noisy input with activity. The source contains an unfinished template followed by a complete answer; the preparation adapts the answer and labels it accordingly. Claims about universally returning to the nearest stable state or explaining perception are replaced with a bounded numerical interpretation.

## Optional two-bump exercise

Initialise two Gaussians of amplitude 0.3 at +/-pi/4 in a 256-neuron network, then evolve without input for duration 200. The complete answer is used. The rate normalisation does not imply a universal steady u amplitude of 1/sqrt(k), and merging or winner-take-all behaviour should be observed rather than guaranteed. Initialising r is consistent bookkeeping; the update recalculates it from u before recurrent input is used.

## Further questions from the source

- How should distances and connections change for another feature-space topology? A sphere S2 is a two-dimensional surface embedded in three dimensions.
- How might a model relate to head-direction, place or grid representations? Such links need model-specific evidence, not simple one-to-one labels.
- How could asymmetric connectivity or input cause activity to move, and how might velocity signals enter a model?
- What additional connectivity or dynamics might support multiple stable bumps? The original suggestion is a prompt for further study, not an implemented mechanism here.

Parameter sweeps, alternative geometries and biological validation were not added as completed work. Add workshop/provider and starter-code attribution before public sharing.
