# S-Curve Motion Profile for VEX V5

This project implements an  **S-Curve Motion Profile** in **VEXcode V5 Blocks** to enable smooth, accurate, and dynamically-scaled robot movement in autonomous mode.

## 📌 Features

- **Dynamic Phase Allocation**  
  Automatically splits motion into acceleration, cruise, deceleration, and a final constant-speed phase based on travel distance.

- **Exponential Deceleration**  
  Uses functions for smooth velocity tapering, avoiding jerky stops and improving scoring accuracy.

- **Adaptive Velocity Control**  
  Adjusts `TopSpeed` and `MinVelocity` according to the input distance. Shorter paths move slower and avoid full speed ramp-up.

- **Modular My Block Structure**  
  - `CalcAccelDecelExp`: Computes phase lengths & speed thresholds  
  - `CalcVelocityExp`: Calculates target velocity at each moment  
  - `MoveS_CurveExp`: Executes motion with intake option

- **Precision Tuning**  
  Final few inches are covered at a set `MinVelocity` (10%–20%), ensuring consistent stops and alignment.

- **Direction Control + Intake Support**  
  Backward movement and optional intake.
