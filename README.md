# Jupyter‑based Robot Visualization Interface (Part 2)

In **Part 2** of the assignment, the Jupyter Notebook interface is extended to include real-time **visualization** and **statistics** tracking using `matplotlib.animation.FuncAnimation`. This builds on the previous interface, while adding live feedback about the robot's movement and its performance in reaching targets.

The updated notebook now includes:

- An interface to **assign** or **cancel** a target `(x, y)` goal using `ipywidgets`.
- Live data showing the robot’s **current position** and the **distance to the nearest obstacle**.
- A real-time animated plot showing the **robot’s movement** through the environment.
- A bar chart that tracks the **number of reached and not-reached goals**.

## How to use it

### 1. Clone the repository

```bash
git clone https://github.com/CarmineD8/assignment_2_2024.git
cd assignment_2_2024
```

### 2. Build the Catkin workspace

```bash
catkin_make
source devel/setup.bash
```

### 3. Launch the core ROS nodes

```bash
roslaunch assignment_2_2024 assignment1.launch
```

### 4. Clone the notebook interface repository

```bash
git clone https://github.com/AlessandroMangili/assignment2_rt2
cd assignment2_rt2
git switch partII
```

### 5. Start the Jupyter interface

```bash
jupyter notebook
```

If you’re using Docker:

```bash
jupyter notebook --allow-root
```

### 6. Interact with the interface

Open the notebook `action_client_ass2.ipynb` and run all cells. You can use the dropdown menu to choose between **Set a new goal**, **Cancel a goal**, or **Quit the program**.

At the bottom of the notebook, you'll find two key visualizations:
- The **Robot Position Plot**, animated in real time using `FuncAnimation`, shows the robot's current trajectory. The axes are inverted to match the map's coordinate system.
- The **Target Statistics Plot** displays how many targets were successfully reached versus how many were not, updating as the robot navigates.

### 7. Service interface

Optionally, you can also run the `retrieve_goal_ass2.ipynb` notebook. It includes a button to retrieve and display the last goal that was set.