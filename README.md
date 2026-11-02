# Rotation Explorer

An interactive 3D tool for learning and comparing rotation representations
used in robotics, aerospace, and computer graphics.

🔗 **[Upstream Demo](https://sahand1807.github.io/rotation-explorer)**
(does not include this fork's ROS coordinate fixes)

## ROS coordinate convention

This fork uses the right-handed body frame from
[ROS REP-103](https://github.com/ros-infrastructure/rep/blob/master/rep-0103.rst):
**X forward, Y left, Z up**. The camera orbits with Z up, the ground lies in
the XY plane, and the directional models are aligned with the body axes.
The camera model also uses this body frame; it does not use the separate
ROS optical frame convention.

From the zero orientation, positive roll about X lowers the right side,
positive pitch about Y tilts the nose down, and positive yaw about Z turns
left (counterclockwise when viewed from above).

The default body-axis Z→Y→X sequence is equivalent to fixed-axis X→Y→Z
roll, pitch, yaw: `R = Rz(yaw) * Ry(pitch) * Rx(roll)`. Other selectable
orders are provided for comparison. Named RPY presets assign angles by
axis regardless of the selected order.

The learning controls display degrees (°) and convert to radians for
calculation. ROS angle messages normally use radians (rad).

## Features

- **Euler Angles** — body/space conventions, six Tait–Bryan rotation orders
  (ZYX, XYZ, YXZ, XZY, ZXY, YZX), φ/θ/ψ labeling, gimbal lock detection,
  intermediate frames
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
