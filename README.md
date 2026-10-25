# RTL-Power-Estimation

A Perl and Tcl/Tk tool that estimates power for Verilog designs at the RTL stage, before synthesis, so high-power modules can be spotted early.

## Features
- Tcl/Tk GUI for entering parameters and loading a Verilog file
- Perl-based Verilog parsing
- Analytical estimates of dynamic, leakage and clock power
- Toggle-factor heuristics and technology-dependent parameters
- Selectable technology nodes (e.g., 180 nm, 90 nm, 45 nm)
- Reports exported as CSV and text
- Highlights the highest-power modules

## Requirements
- Perl
- Tcl/Tk
- A Verilog file to analyze (e.g., `top_module.v`)

## Usage
1. Launch the Tcl/Tk GUI.
2. Enter the clock frequency, supply voltage and technology node.
3. Load your Verilog file.
4. Click **Run**.
5. Open the generated reports.

## Output
| File | Contents |
|---|---|
| CSV report | Detailed power data per module |
| Text report (`power_report.txt`) | Readable power summary |
| Log file | Run messages and errors |

A power vs. supply voltage plot is included as `vdd_vs_power.png`.

## Example
- Input file: `test.v`
- Clock: 1.0 GHz
- Voltage: 12 V
- Technology node: 32 nm
- Result: `power_report.txt`
