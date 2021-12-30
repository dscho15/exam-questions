Question:

Definition of a grasp (focus on) 
- Disturbance, how to maintain a grasp, closure grasp.
- Definition of a point contact

Answer:

- A mathematical model of grasping is one way of definining a grasp, we resort to two model-types form closure and force closure. They are defined as follows:

1) Form closure if it is impossible to move the object, even infinitesimally, relatively to the grasping device.

2) Force closure is similar to form closure, but relaxed to allow frictional forces to help balance the object wrench.

3) In general, it is desirable to maintain contact, between the object and the grasping device, i.e., no seperation and no unwanted sliding.

4) It is desirable to feedback linearize disturbance forces, i.e., inertia (in case of fast motion) or gravity induced forces.

5) To model force and velocity transmissions, between object and grasping device, we need to model the contact points, usually done by a tangential plane and a normal vector. Three models are considered here: PCWF, HF and SF.

- Grasp maintenance means that the contact forces applied by the hand prevents contact seperation and unwanted contact sliding.

- A closure grasp is defined as a class of grasps that can be maintained for every possible disturbance load.

- A contact point is considered as two coincident points; one on the hand and one on the object.


---

- Delete define roadmap

---

Change constrained sampling to:

Q: 
Constraint sampling -

- Definition of a constraint
- Describe, how it can be applied for motion planning.

A:
- A task constraint is defined by a diagonal selection matrix (1 or 0), depending on whether the constraint is active or not. 
- We want to ensure that the constraints are held, i.e., when proposing new configurations in a probabilistic planner, they should always hold the constraints, i.e., the task-space-error should be close to zero.
- Random Gradient Decent, is a naive approach where random sampling is utilized to ensure a task-space-error of zero.
- Another way of ensuring this, is by sampling in the nullspace of a jacobian which only impose velocities in un-constrained axes. One method is First-Order Retraction.

---

Change answer of

What is the shape of the project matrix P? degrees of freedom? Units?

Q:
What is the shape of the project matrix P? degrees of freedom? Units?

A:
- P is a 3x4 matrix, which can be decomposed into \( K * A * [R | t] \)
- t is the world position in the camera frame (3 dof)
- R is the world position in the camera frame (3 dof)
- K is composed of \( f_u, f_v, s * f, \delta_u, \delta_v \)
- where \(f_u \) describes the focal length [m] times the number of pixels pr. meter in the horizontal axis u. (1 dof)
- where \(f_v \) describes the focal length [m] times the number of pixels pr. meter in the vertical axis v. (1 dof)
- where \( s \) is the skew ratio pixels times the focal length. (1 dof)
- \( \delta_u \) is the offset from the principle point in the horizontal axis u. (1 dof)
- \( \delta_v \) is the offset from the principle point in the horizontal axis v. (1 dof)
- 11 dof total.

---
Change

Q: What probability does a particle filter represent? How does it represent a density?

To

Q:
How are probability density functions represented in particle filters?

A:
- It is represented by the state, i.e., location: \(x, y\) and their weight: w (representing the states probability).
- With a lot of particles, we are able to represent the true posterior pdf given by (measurements and prediction).


---

Q: Motion Planning

Reformulate

Q: Mention four criterias that can characterize motion planning types.

---

Remove

Holonomic System


---

Q:
What is the complex conjugate of a quaternion?

Reformulate

Q:
How to compute the conjugate of a quaterion? How to multiply? Norm?

- Negate complex part
- Multiply each element of left on all elements of right
- Norm is basically dividing all elements with the euclidean distance

---

Remove

Q:
How does the outlier removal method in point cloud processing work?

Reformulate

Q:
How does the outlier removal method we discussed in class work? (Statistically motivated.)

---

Remove:

Explain similarity matching methods

---

Q:
Safety systems in collaborative robotics

Reformulate to

Q:
Mention some safety systems in collaborative robotics and how they can be defined in terms of four criterias

Answer:

The four criterias are: the speed of robot, the torques of the robot, what does the operator control and what technique is used to ensure this.

- Safety rated monitored stop (Zero, Gravity None, No motion in the presence of operator)
- Hand guiding (Safety rated, directed by operator input, emergency stop / enabling bottom, motion only be direct operator input)
- Speed and seperation monitoring
- Power and force limiting

With image

---

What is an aspect graph? (Remove)

---

Update:

How does an aspect graph work?

- A hierarchical clustering graph that seeks to speed up template matching by clustering templates with similar view-points.
- The clustering works by clustering similar view points in a coarse(top of tree)-to-fine(leaves of tree) grained manner. 
- When an image is recieved; we traverse the tree with highest similarity score corresponding to the most coarse-level-match.
- That match correspondence to a cluster of templates, which represents other clusters of viewpoints ideally.


---

Remove

Q:
How would you choose the base of a manipulator