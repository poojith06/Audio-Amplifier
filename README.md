# Audio Amplifier

This repository contains the LTspice design files for a multi-stage audio amplifier.

The project is organized as a four-stage signal chain:

1. Preamplifier stage for weak input signals.
2. Gain stage for additional voltage amplification and biasing.
3. Active band-pass filter to keep the desired audio range and reduce noise.
4. Power amplifier stage to drive the output load.

The design was analyzed theoretically, verified through simulation, and documented in the report stored in the `Report/` folder.

## Repository Structure

```text
LTspice/
  1st-stage(pre_amp).asc
  2nd-stage(gain).asc
  3rd-stage(BPF).asc
  4th-stage(pow_amp).asc
  final_ckt.asc
  tip31a.lib
  tip32a.lib
  UA741.lib
Report/
  Report.pdf
```

## Circuit Files

- `1st-stage(pre_amp).asc` - first amplification stage.
- `2nd-stage(gain).asc` - transistor gain stage.
- `3rd-stage(BPF).asc` - active band-pass filter stage.
- `4th-stage(pow_amp).asc` - class AB power stage.
- `final_ckt.asc` - combined final circuit.

## Simulation Notes

- Open the desired `.asc` file in LTspice.
- Keep the library files (`UA741.lib`, `tip31a.lib`, `tip32a.lib`) in the same `LTspice/` folder so the symbols can resolve correctly.
- Run the transient analysis already defined in the schematic.
- For the filter stage, the report also discusses AC response and cutoff frequencies.

## Project Summary

The amplifier is designed to process low-amplitude audio signals through a preamp, gain stage, active filter, and power stage. The final circuit was validated in simulation and then implemented in hardware.

## Report

The full write-up, calculations, and results are in `Report/Report.pdf`.

## Requirements

- LTspice installed
- The included library files available alongside the schematic files