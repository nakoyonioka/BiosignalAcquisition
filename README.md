# Multi-Channel Biosignal Acquisition System with DRL

This project provides a hardware platform for capturing physiological signals such as EEG or ECG. It features multiple input channels with dedicated analog signal conditioning stages (amplification, filtering) to prepare the signals for digitization. A key aspect is the inclusion of a Driven Right Leg (DRL) circuit on Channel 1, a common technique in biopotential measurements to improve signal quality by reducing common-mode interference. The system also incorporates robust power management, supporting battery operation and providing necessary regulated voltage rails, before signals are passed to an Analog-to-Digital Converter (ADC) for digital processing via either isolated or non-isolated SPI.

## Features

- **Multi-Channel Input:** Supports acquisition from 4 independent biosignal channels.
- **Analog Front-End:** Each channel includes amplification and filtering stages (high-pass and low-pass filters).
- **Driven Right Leg (DRL):** Channel 1 features a DRL circuit for enhanced common-mode noise rejection.
- **Signal Conditioning:** Band-pass filtering.
- **Analog-to-Digital Conversion:** Utilizes an onboard ADC (**AD7682BCP**) to convert analog signals to digital data.
- **Digital Interface:** Provides SPI communication interface for connecting to a microcontroller or processor. Includes options for isolated or non-isolated SPI.
- **Power Management:**
  - Battery input and switching.
  - Battery protection IC (BQ29723).
  - Boost converter (TPS61232) for generating +5V from a lower battery voltage.
  - RED3025 and LM2776 IC for generating reference voltagse for ADC and opamps
  - Virtual ground generation for the analog circuitry.
