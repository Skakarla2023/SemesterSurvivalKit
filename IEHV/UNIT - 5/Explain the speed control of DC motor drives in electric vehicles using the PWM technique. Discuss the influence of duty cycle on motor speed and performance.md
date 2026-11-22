# Explain the speed control of DC motor drives in electric vehicles using the PWM technique. Discuss the influence of duty cycle on motor speed and performance.

- A DC motor is an electrical machine that converts electrical energy (DC supply) into mechanical energy (rotational motion).
- In an Electric Vehicle (EV), the motor rotates the wheels and helps the vehicle move.
- But do we always need the motor to run at the same speed?
  - When the vehicle starts, we need low speed.
  - When the vehicle accelerates, we need higher speed.
  - When the vehicle slows down, we need to reduce motor speed.
- So, we need a method to control the speed of the motor.
- One commonly used method is PWM (Pulse Width Modulation).

## PWM

- PWM is a technique used to control the speed of a DC motor by changing the amount of voltage supplied to it.
- Instead of continuously changing the supply voltage, PWM switches the power supply ON and OFF very quickly.
- By changing the ON time and OFF time, we can control the average voltage supplied to the motor.
- Important terms:
  - ON time (Ton): Time during which the power supply is connected to the motor.
  - OFF time (Toff): Time during which the power supply is disconnected.
  - Duty Cycle: Percentage of time the supply remains ON during one switching cycle.
  - Switching Frequency: Number of ON-OFF cycles per second.

### Working

The working is simple:
1. When the switch is ON, the battery supplies power to the motor.
2. When the switch is OFF, the supply is disconnected.
3. This ON-OFF process happens very quickly.
4. By changing the ON time, we control the average voltage supplied to the motor.
5. The motor speed changes according to the average voltage.

<img width="535" height="280" alt="image" src="https://github.com/user-attachments/assets/05e17202-e3f9-4258-9326-4282b7a472de" />

### Influence of Duty Cycle:

- **Low duty cycle:** Low average voltage and low motor speed.
- **Medium duty cycle:** Medium average voltage and medium motor speed.
- **High duty cycle:** High average voltage and higher motor speed.
