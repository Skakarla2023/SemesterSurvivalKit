# Discuss various electric drive-train topologies based on power-source configuration with suitable diagrams.

- It explains how different power sources are arranged and connected to supply energy to an electric vehicle (EV).
- Power-source configuration means the arrangement of energy sources such as batteries, fuel cells, supercapacitors, or an IC engine to supply power to the electric motor.
- There are 5 types of drive train topologies based on power-source configuration:
  1. Battery only configuration
  2. Battery + Fuel cell configuration
  3. Battery + supercapacitor configuration
  4. Battery + IC Engine configuration
  5. Battery + solar energy configuration
 

###  1. Battery only configuration

- The battery is the only energy source.
- It stores electrical energy and supplies it to the motor.
- The inverter converts DC power into AC power when required.
- The motor converts electrical energy into mechanical energy to drive the wheels.

```txt
 Battery
   |
 Inverter
   |
 Electric Motor
   |
  Wheels
```


###  2. Battery + Fuel cell configuration

- The fuel cell converts hydrogen energy into electrical energy.
- The fuel cell supplies power mainly during normal driving.
- The battery stores energy and provides extra power during acceleration.
- During braking, regenerative braking can recharge the battery.

```txt
       Hydrogen
          |
      Fuel Cell
          |
     DC-DC Converter
          |
     ┌────┴─────┐
     │          │
   Battery   DC Bus
     │          |
     └────┬─────┘
          |
       Inverter
          |
        Motor
          |
        Wheels
```

###  3. Battery + supercapacitor configuration

- The battery supplies energy for normal driving and long-duration operation.
- The supercapacitor supplies extra power during sudden acceleration.
- During regenerative braking, energy recovered from braking can be stored in the battery or supercapacitor.
- The DC-DC converter controls the power flow.

```txt
       Battery
          |
       DC-DC
      Converter
          |
     ┌────┴────┐
     │ DC Bus  │ ← Supercapacitor
     └────┬────┘
          |
       Inverter
          |
       Motor
          |
        Wheels
```

###  4. Battery + IC Engine configuration

- This configuration uses both an IC engine and an electric motor.
- The engine uses fuel to produce mechanical power.
- The battery supplies electrical power to the motor.
- The engine and motor can work separately or together, depending on the hybrid system.
- The battery can also be charged through regenerative braking.

```txt
          Fuel Tank
              |
          IC Engine
              |
              ├──────────────→ Wheels
              |
          Generator
              |
           Battery
              |
        Electric Motor
              |
             Wheels
```

###  5. Battery + solar energy configuration

- Solar panels convert sunlight into electrical energy.
- The solar controller regulates the power supplied to the battery.
- The battery stores the energy.
- The motor uses the stored energy to drive the wheels.

```txt
      Solar Panels
           |
   Solar Controller
           |
        Battery
           |
        Inverter
           |
         Motor
           |
         Wheels
```
