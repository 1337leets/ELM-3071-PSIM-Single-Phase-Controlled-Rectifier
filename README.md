# ELM-3071-PSIM-Single-Phase-Controlled-Rectifier
Phase-controlled single-phase full-wave rectifier designed in PSIM for ELM-3071 Power Electronics. Includes gate firing circuit design, simulation report, and an alternative single-source control implementation.

## Design

- Input: 85 V rms, 50 Hz
- Firing angle: α = 60°
- Thyristor full bridge (T12 / T34) with a resistive load and an optional output filter capacitor
- Gate control: a zero-crossing comparator on the source voltage picks the half cycle, a sawtooth compared against a DC reference sets α, and two AND gates route the firing pulse to T12 or T34

Expected average output voltage:

```
Vm = 85 · √2 = 120.208 V
Vd = (Vm / π) · (1 + cos α) = 57.395 V
```

## Versions

| Folder / file | Course | Notes |
|---------------|--------|-------|
| `1P-Contolled-FW-Rectifier.psimsch`, `Project Report.pdf` | ELM-3071 Power Electronics I (Fall 2025/26) | Full assignment: also includes THD, power factor and the capacitor-filtered case |
| `1P-Contolled-FW-Rectifier_PSIM-9.0.3.psimsch` | ELM-3071 | Same assignment, saved for PSIM 9.0.3 |
| `only main ac source.psimsch` | ELM-3071 | Alternative control that runs from the single main AC source |
| `lab/` | Power Electronics I Lab (Spring 2025/26) | Lab version of the same rectifier; the circuit was also built and tested in the lab experiment |

The lab assignment repeats the rectifier with the same input voltage and
firing angle, but its component values can differ from the course version.
Its report covers the output voltage, input power and unity-power-factor
current calculations with the simulation waveforms.

## Tools
PSIM
