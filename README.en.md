# PureVision VLN | Multi-view Pure-Vision Language Navigation

[中文版](README.md)

This is an evolving showcase of multi-view pure-vision language navigation. The system uses visual observations and natural-language instructions to perform cross-area navigation, semantic object search, and passage through structured environments.

With a small set of scene-level demonstrations, the system can align spatial context, language goals, and continuous actions, showing practical generalization to new instructions and related environments.

## Current demos

- Indoor cross-area navigation: living room to kitchen.
- Semantic object search: bed, wooden wardrobe, and water dispenser. The water-dispenser demos include both lights-on and lights-off test scenes; training used only lights-on scene data.
- Structured passage: moving through an access gate.

## Simulation evaluation

After the real-robot results, the page presents seven representative closed-loop simulation evaluations. They cover outdoor grass bypass/crossing, indoor cross-area navigation, precise STOP, and recovery from initial heading perturbations of ±75°. Simulation footage is clearly separated from real-robot video and includes SPL, final error, and collision counts.

These videos are closed-loop online evaluations after training, not training samples. The model continuously predicts local waypoints and STOP while the controller executes those predictions.

## Live page

GitHub Pages: `https://tangyipeng100.github.io/multiview-vln-showcase/`

New videos and scenarios will be added as the project develops.
