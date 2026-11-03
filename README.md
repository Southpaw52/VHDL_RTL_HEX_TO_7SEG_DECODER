# Hexadecimal to Seven-Segment Decoder

**Author: southpaw**

A combinational VHDL design converting a four-bit hexadecimal input into
seven active-high segment signals.

| Input | Output | Display convention |
|---|---|---|
| hex_in(3 downto 0), 0–F | seg_out(6 downto 0), a–g | Common cathode |

## Implementation

[HexTo7Seg.vhd](HexTo7Seg.vhd) implements the segment mapping using Boolean
expressions. The repository contains one RTL implementation; a separate
case-based implementation is not included.

## Files

| File | Purpose |
|---|---|
| [HexTo7Seg.vhd](HexTo7Seg.vhd) | Decoder RTL |
| [HexTo7Seg_TB.vhd](HexTo7Seg_TB.vhd) | Input stimulus for simulation |
| [simulation_waveform.png](simulation_waveform.png) | Historical waveform image |

## Simulation evidence

![Historical decoder simulation waveform](simulation_waveform.png)

The supplied testbench cycles inputs but does not assert expected outputs.
The image is historical evidence, not a newly executed exhaustive check.
No simulation, synthesis or hardware test was run for this documentation update.

## Hardware integration

FPGA board constraints, pin assignments, display drivers and current-limiting
components are outside this repository. Supply those for the actual board
before using the design with a physical display.

## Authorship and licensing

Coursework implementation: **southpaw**.
Application code is MIT-licensed (see LICENSE); third-party components keep their own licenses.
