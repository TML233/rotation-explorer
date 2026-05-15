# Rotation Explorer

An interactive 3D tool for learning and comparing rotation representations
used in robotics, aerospace, and computer graphics.

🔗 **[Live Demo](https://sahand1807.github.io/rotation-explorer)**

## Features

- **Euler Angles** — body/space conventions, all rotation orders (ZYX, XYZ, 
  ZXZ, ...), φ/θ/ψ labeling, gimbal lock detection, intermediate frames
- **Rotation Matrix** — editable 3×3 SO(3) input, orthogonality validation, 
  Gram-Schmidt orthogonalization, axis-angle extraction
- **Quaternion** — axis-angle and raw component input, live formula breakdown 
  showing how w/x/y/z are derived from θ and n̂, SLERP interpolation
- **Compare** — side-by-side property table, interactive gimbal lock demo, 
  numerical drift simulation, composition cost analysis
- **6 interchangeable 3D models** — aircraft, drone, cube, satellite, camera, rocket
- Fully connected — changing any representation updates all others in real time


## Background

Built as an educational tool for understanding the trade-offs between 
rotation representations, particularly relevant to control systems, 
robotics, and attitude estimation.