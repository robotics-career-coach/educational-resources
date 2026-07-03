# Simulation

Resources for Gazebo, Isaac Sim, MuJoCo, and other robot simulators — test and iterate on robot behavior without physical hardware.

## Gazebo

- **Gazebo Simulation Tutorials (latest)** — Open Robotics
  https://gazebosim.org/docs/latest/tutorials/
  The official tutorials for the current Gazebo simulator covering building robots in SDF, sensors, actors, and the GUI.

- **Setting up a robot simulation (Gazebo)** — ROS 2 Documentation
  https://docs.ros.org/en/jazzy/Tutorials/Advanced/Simulators/Gazebo/Gazebo.html
  Official ROS 2 tutorial on integrating Gazebo with ROS 2. For Jazzy, the recommended paired simulator is Gazebo Harmonic.

- **Gazebo Simulation tutorial** — Articulated Robotics (Josh Newans)
  https://articulatedrobotics.xyz/tutorials/mobile-robot/concept-design/concept-gazebo/
  A clear, practical community tutorial walking through spawning a URDF robot into Gazebo and driving it with ROS 2.

## MuJoCo

- **MuJoCo Documentation** — Google DeepMind
  https://mujoco.readthedocs.io/
  The canonical reference for MuJoCo (overview, MJCF modeling, computation, Python bindings). Thorough but reference-style, so pair with a tutorial for beginners.

- **google-deepmind/mujoco (GitHub)** — Google DeepMind
  https://github.com/google-deepmind/mujoco
  The main C/C++ source repository with Python bindings, releases, and links to Colab notebooks. Apache 2.0.

- **MuJoCo Python Tutorial (Colab)** — Google DeepMind
  https://colab.research.google.com/github/google-deepmind/mujoco/blob/main/python/tutorial.ipynb
  The official introductory notebook using the native Python bindings — covers MJCF basics, simulation, rendering, and contacts. The best zero-setup starting point.

- **MuJoCo MJX Tutorial (Colab)** — Google DeepMind
  https://github.com/google-deepmind/mujoco/blob/main/mjx/tutorial.ipynb
  Introductory tutorial for MuJoCo XLA (MJX), the JAX-based implementation for GPU/TPU-accelerated RL training; trains humanoid and quadruped locomotion with Brax PPO. Requires a GPU Colab runtime.

- **dm_control Tutorial (Colab)** — Google DeepMind
  https://colab.research.google.com/github/google-deepmind/dm_control/blob/main/tutorial.ipynb
  Introductory notebook for dm_control, DeepMind's RL environment stack on top of MuJoCo.

- **google-deepmind/dm_control (GitHub)** — Google DeepMind
  https://github.com/google-deepmind/dm_control
  DeepMind's software stack for physics-based simulation and RL environments using MuJoCo: includes the Control Suite, PyMJCF (procedural model authoring), Composer, and an interactive viewer.

- **google-deepmind/mujoco_menagerie (GitHub)** — Google DeepMind
  https://github.com/google-deepmind/mujoco_menagerie
  A curated collection of high-quality, ready-to-use robot models (quadrupeds, manipulators, dexterous hands, humanoids) that work out of the gate. Each model has its own license.

- **Gymnasium MuJoCo Environments** — Farama Foundation
  https://gymnasium.farama.org/environments/mujoco/
  The standard RL benchmark environments (HalfCheetah, Ant, Humanoid, Hopper, etc.) built on MuJoCo; `pip install gymnasium[mujoco]`. The default way to connect MuJoCo to RL.

- **Stable-Baselines3 Documentation** — Antonin Raffin et al.
  https://stable-baselines3.readthedocs.io/
  Reliable implementations of RL algorithms (PPO, SAC, A2C, DQN) that plug directly into Gymnasium-MuJoCo environments; includes examples and Colab notebooks. MIT license.

- **MuJoCo Playground** — Google DeepMind / UC Berkeley (Kevin Zakka, Carlo Sferrazza, Pieter Abbeel et al.)
  https://github.com/google-deepmind/mujoco_playground
  An open-source library of GPU-accelerated environments for robot learning and sim-to-real, built on MJX (locomotion, manipulation, DM Control Suite, vision). Trains in minutes on a single GPU. Apache 2.0. Project site: https://playground.mujoco.org/

- **google/brax (GitHub)** — Google
  https://github.com/google/brax
  A fully differentiable, massively parallel physics engine in JAX with built-in RL algorithms (PPO etc.); interoperates with MJX. Apache 2.0.

- **MuJoCo Python Tutorials (playlist)** — Pranav Bhounsule (UIC)
  https://www.youtube.com/playlist?list=PLc7bpbeTIk75dgBVd07z6_uKN1KQkwFRK
  Step-by-step beginner playlist teaching the official MuJoCo Python bindings with short videos and new examples. Companion site: https://pab47.github.io/mujocopy.html

- **MuJoCo Bootcamp / ME 392: Robotics with MuJoCo** — Pranav A. Bhounsule, University of Illinois at Chicago
  https://pab47.github.io/mujoco.html (bootcamp) and https://pab47.github.io/mujoco2022.html (12-week course)
  A senior-undergrad/first-year-grad course teaching robotics fundamentals in MuJoCo: forward/inverse kinematics, planar dynamics, position/velocity/torque control, finite state machines, and MJCF/XML modeling. The most beginner-friendly university resource.

- **CS 285: Deep Reinforcement Learning** — Sergey Levine, UC Berkeley
  https://rail.eecs.berkeley.edu/deeprlcourse/
  Graduate deep RL course (imitation learning, policy gradients, Q-learning, actor-critic, model-based & offline RL) whose assignments train neural nets in PyTorch on MuJoCo control tasks. Intermediate/advanced.

- **CS 224R: Deep Reinforcement Learning** — Stanford University
  https://cs224r.stanford.edu/
  Applied deep RL with emphasis on robotics and motor control (imitation learning, offline RL, goal-conditioned RL, meta-RL); assignments typically use MuJoCo continuous-control environments. Intermediate/advanced.

- **tayalmanan28/MuJoCo-Tutorial (GitHub)** — Manan Tayal
  https://github.com/tayalmanan28/MuJoCo-Tutorial
  Step-by-step Jupyter notebooks (run in Colab or locally) to get started with the modern open-source MuJoCo Python package.

- **BolunDai0216/PyMuJoCoBase (GitHub)** — Bolun Dai
  https://github.com/BolunDai0216/PyMuJoCoBase
  Starter code and examples for MuJoCo simulations with keyboard/mouse callbacks via the Python bindings; translates Bhounsule's MuJoCo Bootcamp C examples into Python.

## NVIDIA Isaac Sim

> **Hardware requirement:** Isaac Sim requires an NVIDIA RTX GPU. Minimum: GeForce RTX 3070 (8 GB VRAM); Recommended: GeForce RTX 4080 (16 GB VRAM). GPUs without RT Cores (e.g., A100, H100) are not supported. Newer Isaac Sim versions (5.x) raise the listed minimum to RTX 4080. Learners without an RTX GPU can use NVIDIA Brev (pay-by-the-hour cloud).

- **NVIDIA Isaac Sim — Getting Started Tutorials** — NVIDIA
  https://docs.isaacsim.omniverse.nvidia.com/latest/introduction/quickstart_index.html
  Official quickstart tutorials for the photorealistic, GPU-accelerated robot simulator (GUI, Python scripting, ROS 2 integration).

- **Isaac Sim Basic Usage Tutorial** — NVIDIA
  https://docs.isaacsim.omniverse.nvidia.com/latest/introduction/quickstart_isaacsim.html
  Beginner walkthrough: navigate the GUI, add objects, set physics/material properties, and run your first simulation via three workflows (GUI, extension script, standalone Python).

- **isaac-sim/IsaacSim (GitHub)** — NVIDIA
  https://github.com/isaac-sim/IsaacSim
  Open-source Isaac Sim application repository (Apache 2.0); supports URDF/MJCF/CAD import, PhysX + Newton physics, RTX sensors, ROS 2, synthetic data, and RL.

- **Getting Started With Isaac Lab (learning path)** — NVIDIA
  https://docs.nvidia.com/learning/physical-ai/getting-started-with-isaac-lab/latest/index.html
  A free, structured, multi-module path: intro to robot learning, the NVIDIA simulator ecosystem, "Train Your First Robot" (cartpole RL), and "Train Your Second Robot" (UR10 + gripper). The single best free, structured on-ramp for Isaac Lab.

- **Physical AI / Robotics Fundamentals Learning Path** — NVIDIA
  https://www.nvidia.com/en-us/learn/learning-path/robotics/
  Curated path spanning OpenUSD, Omniverse, Isaac Sim, Isaac Lab, and Isaac ROS, with per-module level and time estimates. Individual DLI courses vary free vs. paid.

- **Assemble a Simple Robot in Isaac Sim (DLI mini-course)** — NVIDIA Deep Learning Institute
  https://learn.nvidia.com/courses/course-detail?course_id=course-v1:DLI+T-OV-01+V1
  A free self-paced mini-course on the Isaac Sim interface and basic robot assembly. Requires a free NVIDIA Developer account.

- **Introduction to Robotic Simulations in Isaac Sim (DLI)** — NVIDIA Deep Learning Institute
  https://learn.nvidia.com/courses/course-detail?course_id=course-v1:DLI+S-OV-03+V1
  Beginner DLI course covering building a simple robot, physics properties, sensors, and troubleshooting. Check price field — some DLI courses are free, others are paid.

- **Isaac Lab Documentation** — NVIDIA
  https://isaac-sim.github.io/IsaacLab/main/
  Official docs for the GPU-accelerated robot-learning framework built on Isaac Sim: 16+ robot models, 30+ environments with ready-to-train implementations, tutorials, and RL training guides.

- **isaac-sim/IsaacLab (GitHub)** — NVIDIA
  https://github.com/isaac-sim/IsaacLab
  The Isaac Lab framework source (BSD-3-Clause). Trainable with RSL-RL, SKRL, RL-Games, and Stable-Baselines3. Locomotion recipes span 11 robot morphologies including Anymal, Spot, Go1/2, and Cassie.

- **isaac-sim/IsaacLabTutorial (GitHub)** — NVIDIA
  https://github.com/isaac-sim/IsaacLabTutorial
  Official tutorial repo designed to accompany the Isaac Lab docs; each branch represents a stage of the tutorial project. Apache 2.0.

- **Isaac Lab Tutorials (docs index)** — NVIDIA
  https://isaac-sim.github.io/IsaacLab/main/source/tutorials/index.html
  Step-by-step Python tutorials: spawning objects, articulations, manager-based and direct RL environments, sensors, and motion generators.

- **ROS 2 Integration (Isaac Sim docs)** — NVIDIA
  https://docs.isaacsim.omniverse.nvidia.com/latest/installation/install_ros.html
  Definitive guide to the Isaac Sim ROS 2 bridge. Compatible with ROS 2 Humble (Ubuntu 22.04) and Jazzy (Ubuntu 24.04, recommended); supports Fast DDS, Cyclone DDS, and Zenoh.

- **ROS 2 Tutorials (Isaac Sim docs)** — NVIDIA
  https://docs.isaacsim.omniverse.nvidia.com/latest/ros2_tutorials/ros2_landing_page.html
  Tutorial series covering ROS 2 bridges, publishing/subscribing sensor data, Nav2 navigation (Carter robot), and ROS 2 launch integration.

- **Getting Started — Isaac ROS** — NVIDIA
  https://nvidia-isaac-ros.github.io/getting_started/index.html
  Isaac ROS (hardware-accelerated ROS 2 GEMs/NITROS) getting-started guide; tested against ROS 2 Jazzy and integrates with Isaac Sim for software-/hardware-in-the-loop. Targets Jetson/RTX hardware.

- **NVIDIA Isaac Sim and Omniverse Tutorials (playlist)** — NVIDIA Omniverse
  https://www.youtube.com/playlist?list=PL2bKqBZg-pzWaX8H_Fk1GqzOBM9XOjGL9
  Official NVIDIA video tutorial playlist for Isaac Sim/Omniverse workflows.

- **shaoxiang/awesome-isaac-sim (GitHub)** — community (shaoxiang)
  https://github.com/shaoxiang/awesome-isaac-sim
  A curated collection of Isaac Sim resources, tutorials, and projects.

- **sjtuyinjie/awesome-isaac-sim (GitHub)** — community (SJTU)
  https://github.com/sjtuyinjie/awesome-isaac-sim
  Curated list documenting the Isaac Gym → Isaac Sim → Orbit → Isaac Lab lineage, with environment repos, ROS 2 workspaces, and example projects.

- **robotlearning123/awesome-isaac-gym (GitHub)** — community
  https://github.com/robotlearning123/awesome-isaac-gym
  Curated list of Isaac Gym/Isaac Sim RL frameworks, papers, and tutorials (locomotion, manipulation, sim-to-real).

## Other Simulators

- **Underactuated Robotics (notes + simulation)** — Russ Tedrake, MIT
  https://underactuated.csail.mit.edu/
  Continuously-updated free course notes with interactive, Drake-based simulation examples for dynamics and control. Lecture videos available on YouTube. (Original 6.832 OCW materials at https://ocw.mit.edu/courses/6-832-underactuated-robotics-spring-2009/ are dated; prefer the continuously-updated notes.)

- **Introduction to Aerial Robotics (ELEC 5660)** — Shaojie Shen, HKUST
  https://github.com/HKUST-Aerial-Robotics/HKUST-ELEC5660-Introduction-to-Aerial-Robotics
  Open-source course notes, lab tutorials, and project Docker files covering rigid-body dynamics, control, trajectory planning, sensor fusion, and vision-based state estimation for autonomous aerial robots.

## Notes

- **MuJoCo** is fully free and open source (Apache 2.0, open-sourced by DeepMind in May 2022). It runs on a CPU/laptop with no GPU required, installs via `pip install mujoco`, and has excellent Colab notebooks for zero-setup learning. It has no official ROS 2 bridge but integrates easily with RL stacks (Gymnasium, Stable-Baselines3). Use MuJoCo for RL/control algorithm learning, and Isaac Sim for full ROS 2 robot-stack simulation.
- **Pre-2022 MuJoCo content is outdated.** Resources referencing `mujoco-py`, `mjkey.txt` license keys, or "mjpro150" predate the open-sourcing and the modern `mujoco` Python package; prefer 2022+ material.
- **Isaac Sim's** code is Apache 2.0 licensed, but running it requires the separately-licensed Omniverse Kit SDK, 3D models, and textures under the NVIDIA Isaac Sim Additional Software and Materials License — so it is open-source code but not unconditionally free of NVIDIA's component terms, and it has substantial GPU hardware requirements.
- **DLI course pricing varies.** Always confirm the price field on each NVIDIA DLI course page — "Assemble a Simple Robot" is confirmed free; others may charge.
- **Gazebo Classic** (Gazebo 11) and all other versions of Gazebo Classic reached official end-of-life on January 31, 2025. OSRF now supports only modern Gazebo (Harmonic LTS, supported until September 2028). Direct efforts to modern Gazebo paired with ROS 2 Jazzy, not Gazebo Classic.
