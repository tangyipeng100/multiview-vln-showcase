# PureVision VLN | Multi-view Pure-Vision Language Navigation

[中文版](README.md)

This is an evolving showcase of multi-view pure-vision language navigation. The system uses visual observations and natural-language instructions to perform cross-area navigation, semantic object search, and passage through structured environments.

With a small set of scene-level demonstrations, the system can align spatial context, language goals, and continuous actions, showing practical generalization to new instructions and related environments.

## Current demos

- Indoor cross-area navigation: living room to kitchen.
- Semantic object search: bed, wooden wardrobe, and water dispenser. The water-dispenser demos include both lights-on and lights-off test scenes; training used only lights-on scene data.
- Structured passage: moving through an access gate.
- Unseen compound instruction: executing “go to the living-room area and find the long white table,” which combines cross-area navigation and semantic object search. This is one real-robot execution and is not presented as validation of all unseen instructions.
- Precise-object exploration: using the same instruction to find a small white plush toy in two scenes. The motion trend points toward the target, but close-range STOP is not yet stable; the effects of target scale and scene texture require more data.
- Elevator interaction: entering, exiting, and generating a directional trajectory according to which elevator door opens. Two new real-robot clips show the robot exiting and stopping near the red circular lobby marker; one includes a person passing near the doorway. The left/right selection video validates visual judgment and trajectory selection only; no movement was executed. Current real-robot results remain `10/11` successful entries and `7/10` successful exits; the new showcase clips were not used to recalculate these figures.

## Simulation evaluation

After the real-robot results, the page presents seven representative closed-loop simulation evaluations. They cover outdoor grass bypass/crossing, indoor cross-area navigation, precise STOP, and recovery from initial heading perturbations of ±75°. Simulation footage is clearly separated from real-robot video and includes SPL, final error, and collision counts.

These videos are closed-loop online evaluations after training, not training samples. The model continuously predicts local waypoints and STOP while the controller executes those predictions.

## Project timeline

- **2026-10-10**: Added a real-robot cross-area object-search case driven by an exact compound instruction absent from training, one executed elevator-entry video, and two elevator-exit clips that stop near the red lobby marker.
- **2026-10-09**: Added two cross-scene precise small-object search comparisons, elevator entry/exit statistics, and another executed elevator-entry trial.
- **2026-10-08**: Added a real-robot elevator-entry case with a limited door cue. Only a small portion of the open doorway is visible to the cameras, yet the robot still generates an entry trajectory and enters the elevator.
- **2026-09-30**: Added elevator entry, exit, and left/right door-selection scenes.
- **2026-09-29**: Published the initial real-world and simulation results, including cross-area navigation, semantic object search, access-gate passage, lighting-condition tests, and closed-loop simulation evaluation.

## Live page

GitHub Pages: `https://tangyipeng100.github.io/multiview-vln-showcase/`

New videos and scenarios will be added as the project develops.
