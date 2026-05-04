# 🦾 Kortex Gen3 Lite - ROS Description Package

This repository contains the standalone ROS description package for the **Kinova Kortex Gen3 Lite** robotic arm. It includes localized meshes, the URDF kinematic model, and necessary configuration files for robot visualization.

---

### 📂 Package Structure
*   **`meshes/`**: Contains the `.STL` files for all arm links (Shoulder, Forearm, Wrist, etc.).
*   **`urdf/`**: Contains the `kortex-gen3-lite.urdf` file defining the robot's kinematic chain.
*   **`resource/` & `test/`**: Standard ROS 2 package directories for metadata and testing.

---

### 🛠️ Installation (As a Package)
To use this package in your own ROS workspace, clone it into your `src` directory:
```bash
# Navigate to your workspace src folder
cd ~/your_workspace/src

# Clone this repository
git clone git@github.com:Emmanuel-Iyoha/kortex-gen3-lite_description.git

# Build the package
cd ..
colcon build --packages-select kortex-gen3-lite_description --symlink-install

# Source the workspace
source install/setup.bash

```
---

### 🚧 Current Status Markdown
```markdown
### 🚧 Current Status
- [x] Initialized as a standalone ROS 2 package.
- [x] Localized STL meshes from the main repository into the `meshes/` directory.
- [x] URDF file updated to reference internal package paths.
- [ ] Add `gazebo` tags for physics simulation.
- [ ] Configure `ros2_control` hardware interfaces.
- [ ] Fine-tune joint velocity and effort limits.
```
### 📝 Notes
*   **Self-Contained**: This package was extracted from the `aurora_core1_task4` submission to act as a lightweight description repo.
*   **Mesh Paths**: All visual and collision tags in the URDF use `package://kortex-gen3-lite_description/meshes/` for maximum portability.
*   **Environment**: Developed and tested on Ubuntu 22.04 with ROS 2 Jazzy Jalisco.