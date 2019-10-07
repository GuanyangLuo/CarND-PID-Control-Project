# **PID Controller** 

---

**PID Controller**

The goals/steps of this project are the following:
* Build a PID controller and tune the PID hyperparameters
* Test the solution on the simulator
* Tune the PID controller until the vehicle can drive successfully around the track
* Make reflections in a write-up file

---

### Reflection

### 1. Describe the effect each of the P, I, D components had in your implementation.

A large Kp (such as Kp = 1) makes the car more reactive to deviation from the lane center, which causes it to over-react and run off the road even when approaching a gradual turn on the track. A small Kp (such as Kp = 0.05) makes the car less reactive and causes it to be unable to appropriately respond to a sharp turn.

Adding Kd helps alleviate the problem of a small Kp. However, too big of a Kd (such as Kd = 50) causes the car to be very twitchy (steering left and right all the time).

Finally, adding Ki helps the car keep close to the centerline when going through a turn (a "drift" in the reference line). A large Ki (such as Ki = 0.01) causes the car to over-compensate and go off-track on a straight section.

### 2. Describe how the final hyperparameters were chosen.

The final hyperparameters were chosen with manual tuning. Using the values from the "PID Control" lecture as a baseline for the order of magnitude, I tried a few values for Kp, Kd, and Ki to create Reflection 1. As I tried those values, I first found a Kp value that works well, then I found Kd, and then I found Ki.