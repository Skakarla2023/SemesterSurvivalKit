# Hybrid Traction

- Hybrid traction is a system in which a vehicle uses two different power sources to drive its wheels, usually:
  - **Internal Combustion Engine (ICE)** – uses petrol or diesel fuel.
  - **Electric motor** – uses electrical energy stored in a battery.
- In a Hybrid Electric Vehicle (HEV), both the engine and the electric motor can provide power to move the vehicle. Depending on driving conditions, the vehicle may use the engine alone, the electric motor alone, or both together.

### Why is Hybrid Traction used?

- reduces fuel consumption.
- increases energy efficiency
- reduces air pollution
- provides better acceleration
- preserves energy during braking


### Block diagram of a hybrid electric vehicle

```txt
       Fuel Tank
           |
           v
       IC Engine
           |
           v
    Power Split Device -------- Battery
           |                       |
           |                 Power Converter
           |                       |
           |                  Electric Motor
           |                       |
           +-----------+-----------+
                       |
                       v
                 Transmission
                       |
                       v
                   Wheels
```


### Components

**1. IC Engine (Internal Combustion Engine)**

- Converts the chemical energy of fuel into mechanical energy.
- Provides power to drive the vehicle.
- Generally uses petrol or diesel.

**2. Electric Motor**

- Converts electrical energy into mechanical energy.
- Helps the vehicle move.
- Provides additional power during acceleration.
- Can also work as a generator during regenerative braking.

**3. Battery Pack**

- Stores electrical energy in chemical form.
- Supplies electricity to the electric motor.
- Stores electrical energy recovered during regenerative braking.

**4. Generator**

- Converts mechanical energy into electrical energy.
- In some hybrid systems, it generates electricity using engine power.
- Helps charge the battery.

**5. Power Converter / Power Electronics**

- Controls the flow of electrical power between the battery, motor and generator.
- An inverter converts DC power from the battery into AC power for an AC motor.
- A DC-DC converter changes one DC voltage level to another.

**6. Transmission System**

- Transfers mechanical power from the engine and/or motor to the wheels.
- Helps provide suitable speed and torque.

**7. Fuel Tank**

- Stores petrol or diesel required by the IC engine.

**8. Hybrid Control Unit (HCU)**

- Acts as the brain of the hybrid vehicle.
- Controls the operation of the engine, motor, battery and generator.
- Decides which power source should be used depending on driving conditions.

**9. Regenerative Braking System**

- Recovers kinetic energy during braking.
- Converts the recovered energy into electrical energy.
- Stores this energy in the battery for future use.


**Working:**

- During starting, the electric motor may drive the vehicle.
- During acceleration, both engine and motor provide power.
- During cruising, the engine may provide most of the power.
- During braking, regenerative braking converts kinetic energy into electrical energy and charges the battery.
