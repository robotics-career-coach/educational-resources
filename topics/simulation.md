# Simulation

Resources for Gazebo, Isaac Sim, and other robot simulators — test and iterate on robot behavior without physical hardware.

## Resources

- **Gazebo Simulation Tutorials (latest)** — Open Robotics
  https://gazebosim.org/docs/latest/tutorials/
  The official tutorials for the current Gazebo simulator covering building robots in SDF, sensors, actors, and the GUI.

- **Setting up a robot simulation (Gazebo)** — ROS 2 Documentation
  https://docs.ros.org/en/jazzy/Tutorials/Advanced/Simulators/Gazebo/Gazebo.html
  Official ROS 2 tutorial on integrating Gazebo with ROS 2. For Jazzy, the recommended paired simulator is Gazebo Harmonic.

- **NVIDIA Isaac Sim — Getting Started Tutorials** — NVIDIA
  https://docs.isaacsim.omniverse.nvidia.com/latest/introduction/quickstart_index.html
  Official quickstart tutorials for the photorealistic, GPU-accelerated robot simulator (GUI, Python scripting, ROS 2 integration).

- **Getting Started With Isaac Sim (learning modules)** — NVIDIA
  https://docs.nvidia.com/learning/physical-ai/getting-started-with-isaac-sim/latest/index.html
  NVIDIA's structured learning path covering robot construction, OmniGraph, URDF import, and ROS 2 integration.

- **Gazebo Simulation tutorial** — Articulated Robotics (Josh Newans)
  https://articulatedrobotics.xyz/tutorials/mobile-robot/concept-design/concept-gazebo/
  A clear, practical community tutorial walking through spawning a URDF robot into Gazebo and driving it with ROS 2.

- **Underactuated Robotics (notes + simulation)** — Russ Tedrake, MIT
  https://underactuated.csail.mit.edu/
  Continuously-updated free course notes with interactive, Drake-based simulation examples for dynamics and control. Lecture videos available on YouTube. (Original 6.832 OCW materials at https://ocw.mit.edu/courses/6-832-underactuated-robotics-spring-2009/ are dated; prefer the continuously-updated notes.)

- **Introduction to Aerial Robotics (ELEC 5660)** — Shaojie Shen, HKUST
  https://github.com/HKUST-Aerial-Robotics/HKUST-ELEC5660-Introduction-to-Aerial-Robotics
  Open-source course notes, lab tutorials, and project Docker files covering rigid-body dynamics, control, trajectory planning, sensor fusion, and vision-based state estimation for autonomous aerial robots.

## Notes

- Gazebo Classic (Gazebo 11) and all other versions of Gazebo Classic reached official end-of-life on January 31, 2025. OSRF now supports only modern Gazebo (Harmonic LTS, supported until September 2028). Direct efforts to modern Gazebo paired with ROS 2 Jazzy, not Gazebo Classic.
- Isaac Sim's code is Apache 2.0 licensed, but running it requires the separately-licensed Omniverse Kit SDK, 3D models, and textures under the NVIDIA Isaac Sim Additional Software and Materials License — so it is open-source code but not unconditionally free of NVIDIA's component terms, and it has substantial GPU hardware requirements.
