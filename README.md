# Load Cell Lab

Load Cell experiment files for calibration, real-time measurement, and validation.

## Repository structure

```text
Loadcell/
├── Model/
│   └── loadcell2569.slx
├── Raw_Data/
│   ├── run1.mat
│   ├── run2.mat
│   └── run4.mat
├── Processed_Result/
│   ├── result_run1.mat
│   ├── result_run2.mat
│   ├── result_run4.mat
│   └── result_final.mat
└── MATLAB/
    ├── plot_mass_vs_adc_separate_runs.m
    └── plot_realtime_adc_staircase_runs.m
```

## Calibration used in the report

Final calibration combines Run 1, Run 2 and Run 4.

- `a_final = 246.9392 count/kg`
- `b_final = -71.3486 count`
- `R² = 0.9986`

```text
ADC = a*m + b
m = (ADC - b)/a
F = m*9.81
```

## Notes

- Run 3 and `run3_but_fall` are not included in the final calibration set.
- `.slxc` is a Simulink cache file and is intentionally excluded.
- `run_up_and_down` is additional data and is not part of the main Run 1/2/4 calibration.
