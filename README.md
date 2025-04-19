# Jupyter‑based Robot Interface (Part 1)

In **Part 1** of the assignment, the original ROS node (an action‑client UI for sending/canceling navigation goals) has been replaced by a **Jupyter Notebook** interface that:

- Lets the user **assign** or **cancel** a target `(x, y)` goal using `ipywidgets`.
- Displays the robot’s **current position** in the environment.
- Shows the **distance** from the robot to the nearest obstacle, updated in real time.

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

### 4. Clone the repository

```bash
git clone https://github.com/AlessandroMangili/assignment2_rt2
cd assignment2_rt2
git switch partI
```

### 5. Start the Jupyter interface

```bash
jupyter notebook
```
If you’re running inside Docker, add:
```bash
jupyter notebook --allow-root
```
### 6. Interact with the interface

This should get your Jupyter‑based action client up and running smoothly. Open the notebook `action_client_ass2.ipynb` in Jupyter and run all cells to start the interface. Once it’s running, select an option from the dropdown menu: **Set a new goal** to send a new `(x, y)` target to the robot, **Cancel a goal** to abort the current navigation, or **Quit the program** to shut down the interface. 
Scroll to the bottom of the notebook to view two live plots: the **Robot Trajectory** plot, which shows the robot’s path on the map (axes are inverted because the origin is at the top‑left corner), and the **Goal Statistics** plot, a bar chart displaying how many goals were reached versus not reached.

### 7. Service interface

If you want, you can also open the `retrieve_goal_ass2.ipynb` notebook. Once it's running, you can interact with it using the provided button, which allows you to retrieve and display the last goal that was set.
