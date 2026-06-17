# Cloud & DevOps for Robotics

Resources for Docker, cloud deployment, and GitHub Actions — the infrastructure that makes robotics software reproducible and deployable.

## Resources

- **Docker Guides — Introduction to GitHub Actions with Docker** — Docker Inc.
  https://docs.docker.com/guides/gha/
  Official step-by-step guide to building and pushing Docker images via a CI/CD pipeline with GitHub Actions.

- **Docker Build GitHub Actions** — Docker Inc.
  https://docs.docker.com/build/ci/github-actions/
  Official reference for Docker's reusable GitHub Actions (build-push, login, buildx, metadata).

- **Creating a Docker container action** — GitHub Docs
  https://docs.github.com/en/actions/sharing-automations/creating-actions/creating-a-docker-container-action
  Official GitHub tutorial on building a containerized custom GitHub Action.

- **Play with Docker Classroom** — Docker
  https://training.play-with-docker.com/
  Free browser-based, hands-on labs and tutorials for learning Docker without local installation.

## Practical Tip

Pair the resources above with the [Henki Robotics ROS 2 repo](https://github.com/henki-robotics/robotics_essentials_ros2) (see [ROS 2 topic](ros2.md)), which ships Docker images for ROS 2. The official ROS 2 docs and ETH course also recommend Docker-based development, making this a natural place to practice containerized robotics CI.
