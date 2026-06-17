# Suggested Learning Path

A staged approach for the cohort, from foundations through capstone integration.

## Stage 1 — Foundations (Weeks 1–4)

Start with core programming and ROS 2 in parallel:
- [CS50P](https://cs50.harvard.edu/python/) (Python) and [learncpp.com](https://www.learncpp.com/) (C++ basics)
- [Pro Git](https://git-scm.com/book/en/v2) for version control
- [Official ROS 2 Tutorials](https://docs.ros.org/en/jazzy/Tutorials.html) and [ETH Zurich Programming for Robotics](https://rsl.ethz.ch/education-students/lectures/ros.html)

**Benchmark:** Every learner can write a Python and a C++ ROS 2 node and push it to GitHub.

## Stage 2 — Core Robotics + Simulation (Weeks 5–8)

Layer in simulation and mechanical fundamentals:
- [Henki Robotics ROS 2 + Gazebo course](https://github.com/henki-robotics/robotics_essentials_ros2) and [official Gazebo tutorials](https://gazebosim.org/docs/latest/tutorials/)
- [Modern Robotics Course 1](https://hades.mech.northwestern.edu/index.php/Modern_Robotics) (free audit) for kinematics
- Begin [FreeCAD](https://www.freecad.org/) or [Onshape](https://learn.onshape.com/) for CAD

**Benchmark:** Learner spawns and drives a simulated robot and models a simple part.

## Stage 3 — Specializations (Weeks 9–14)

Split into focus tracks:
- **Vision:** [CS231n](https://cs231n.github.io/) + [OpenCV docs](https://docs.opencv.org/4.x/d9/df8/tutorial_root.html)
- **ML/RL:** [Andrew Ng ML Specialization](https://www.coursera.org/specializations/machine-learning-introduction) then [Sutton & Barto](http://incompleteideas.net/book/the-book-2nd.html) + [Spinning Up](https://spinningup.openai.com/en/latest/)
- **Embedded:** [Arduino docs](https://docs.arduino.cc/language-reference/) + [CU Boulder courses](https://www.coursera.org/learn/introduction-embedded-systems)
- **DevOps:** [Docker guides](https://docs.docker.com/guides/gha/) + [GitHub Actions](https://skills.github.com/)

**Benchmark:** Each learner completes one perception, one control/RL, and one CI/CD mini-project.

## Stage 4 — Capstone

Integrate via Isaac Sim or Gazebo with a full ROS 2 + Docker + GitHub Actions pipeline.

## Adapting the Path

- If learners struggle with C++/math prerequisites, insert the Modern Robotics math review and delay deep RL.
- If the cohort is already intermediate, compress Stage 1 to one week and move directly to CS231n and Isaac Sim.
