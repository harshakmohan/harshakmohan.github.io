---
title: thoughts on the future of robot manipulation
subtitle: we need fundamental innovation in model architecture and sensor data inputs
---

I am going to outline a technical bet about where I see the landscape shifting for robot manipulation. If we want robots to do useful work and co-exist with humans in the real world, we need fundamental innovation at both the model architecture layer and sensor data input layer.

Learned models will need to be predictive, instead of reactive. Current systems learn a direct mapping from observations to actions, which makes prediction implicit to the model rather than explicit. I believe the next generation of models will be explicit predictive planners, where they can consider many future outcomes conditioned on candidate trajectories.

Currently, monolithic end-to-end architectures are at the center of attention. I believe the industry will move towards modular systems with structured inputs and structured outputs. Monolithic models are hard to debug and hard to observe. This makes them an engineering nightmare for production use-cases. The future robot manipulation stack will look like a modular system with learnable components for processing sensor inputs, predicting and planning next steps, and generating actions.

Models will also need efficient and high-density inputs. I believe we will soon enter the post-RGB-only era. RGB cameras are excellent at providing semantic information about the scene, but they are weak at providing physical state observations about the world. I believe robot manipulation needs sensory inputs that efficiently expose depth, object velocity, and contact forces to reduce the burden on learned models and make the task-specific physical state directly measurable.

In line with this theme, I strongly believe vision is insufficient for the last-centimeter of contact-rich manipulation. Humans can complete precise manipulation tasks with tactile feedback after visually identifying the object and scene of interest. For many fine-grained contact tasks, haptic feedback becomes dramatically more important after contact begins. I believe robots will need some type of tactile or haptic feedback to reliably complete fine-grained contact interactions.

I believe the winning systems will be predictive and modular with multimodal contact-aware inputs. What do you think?
