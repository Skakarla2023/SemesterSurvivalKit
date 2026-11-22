### Power Flow Control in Series-Parallel and Complex Hybrid Configurations

In a Hybrid Electric Vehicle (HEV), power flow control is the process of deciding how power from the IC engine, electric motor, and battery is supplied to the wheels.

The vehicle's control system decides whether to use the engine, motor, or both together depending on driving conditions such as starting, acceleration, cruising, climbing, and braking.

## 1. Power Flow Control in Series-Parallel Hybrid Configuration

A series-parallel hybrid combines the advantages of both series and parallel hybrid systems.
- In series mode, the engine generates electricity through a generator, and the electric motor drives the wheels.
- In parallel mode, the engine directly drives the wheels.
- In combined mode, both the engine and electric motor provide power to the wheels.

<img width="684" height="292" alt="image" src="https://github.com/user-attachments/assets/970feb29-b5b4-44ff-9727-a907724bf0e8" />

### Main Components

- IC Engine: Produces mechanical power using fuel.
- Generator: Converts mechanical power from the engine into electrical power.
- Battery: Stores electrical energy and supplies power to the motor.
- Power converter / inverter: Controls and converts electrical power between the battery, generator and motor.
- Electric motor: Converts electrical energy into mechanical energy to drive the wheels.
- Transmission: Transfers power to the wheels.

### Power Flow Control – Series-Parallel Hybrid

**1. Starting / Low speed**

- Battery supplies power to the motor.
- Motor drives the wheels.
- Engine remains OFF.

**2. Acceleration**

- Engine and motor work together.
- Both supply power to the wheels to increase speed.

**3. Cruising**

- Engine mainly drives the wheels.
- Extra engine power can charge the battery through the generator.

**4. Braking**

- Motor acts as a generator.
- It converts braking energy into electrical energy and stores it in the battery. This is called regenerative braking.



## 2. Power Flow Control in Complex Hybrid Configuration

- A complex hybrid configuration is an advanced hybrid system in which multiple power sources and electrical machines are connected in a more flexible manner.
- It may contain:
  - IC engine
  - Two electric machines (motor-generator 1 and motor-generator 2)
  - Battery
  - Power converters
  - Power-splitting mechanism
  - Transmission
  - Wheels
 

- The two electric machines can perform different functions, and power can flow through multiple paths simultaneously.

### Power Flow Control – Complex Hybrid Configuration

**1. Starting the vehicle**

- Battery supplies power to the motor.
- Motor drives the wheels.
- Engine remains OFF.

**2. Acceleration**

- Engine and motor work together.
- Both provide power to the wheels for faster acceleration.

**3. Cruising**

- Engine mainly drives the wheels.
- One motor may help drive the wheels.
- Another motor may generate electricity to charge the battery.

**4. Battery charging**

- Engine drives the generator.
- Generator produces electricity.
- Electricity is stored in the battery.

**5. Regenerative braking**

- During braking, motor acts as a generator.
- It converts wheel energy into electrical energy.
- This electricity is stored in the battery.

**6. Power splitting**

- Engine power is divided into two paths.
- One path drives the wheels directly.
- Another path generates electricity.
- The electricity can run the motor or charge the battery.


```txt
               Fuel Tank
                   |
                   v
               IC Engine
                   |
                   v
            Power Split Device
              /           \
             /             \
            v               v
     Transmission       Generator
            |               |
            v          Power Converter
          |               |
            |            Battery
            |               |
            |        Power Converter
            |               |
            |          Electric Motor
            |               |
            +-------+-------+
                    |
                    v
                  Wheels
```






<img width="593" height="122" alt="image" src="https://github.com/user-attachments/assets/26dd19c8-ca33-4478-9a49-4898d4297380" />

