# Quadcopter Control System Implementation in Simulink
A Simulink-based implementation of a quadcopter control system using thrust-based altitude control and attitude-based position control.

## Project Overview
The project consists of a single comprehensive Simulink model:
- `quadcopter_model.slx`: Contains both the quadcopter dynamics and control system implementation

The model integrates:
- Complete quadcopter dynamic model
- PID control system
- Thrust-based altitude control
- Attitude-based position control (roll/pitch)

## Requirements
- MATLAB R2020a or newer
- Simulink
- Control System Toolbox
- Aerospace Toolbox (optional, for visualization)

## Model Structure

### Integrated Model Design
The single Simulink model includes:
1. Dynamic System:
   - 6-DOF rigid body dynamics
   - Rotor thrust and torque calculations
   - Gravitational effects
   - Basic aerodynamics

2. Control System:
   - Altitude control via total thrust adjustment
   - Horizontal position control through roll/pitch commands
   - PID controllers for position and attitude

## Getting Started

1. Clone the repository:
```
git clone https://github.com/yourusername/quadcopter-control
```

2. Open MATLAB and navigate to the project directory

3. Open the model:
- `quadcopter_model.slx`

4. Run the simulation:
- Set desired waypoints in the 'Reference Input' block
- Press 'Run' in Simulink
- View results in the scope blocks

## Control Parameters

### Default PID Values
Altitude Control:
- Height control accuracy: ±5cm
- Response time: ~2 seconds

Position Control:
- Maximum roll/pitch: ±15 degrees
- Position accuracy: ±10cm
- Settling time: ~3 seconds

## Usage Notes
- Run `init_simulation.m` before starting the simulation
- Adjust PID gains in the controller blocks if needed
- Monitor system response through provided scope blocks
- Use the visualization block for 3D animation (if available)

## Known Limitations
- Basic aerodynamic effects only
- No wind disturbance modeling
- Simplified motor dynamics
- Limited to near-hover conditions

## Contributing
Feel free to fork this project and submit pull requests. For major changes:
1. Open an issue first to discuss proposed changes
2. Update tests and documentation as needed
3. Ensure all simulations run successfully

## Acknowledgments
- Reference model based on quadcopter dynamics
- Built using MATLAB/Simulink framework
- Inspired by classical control theory applications
