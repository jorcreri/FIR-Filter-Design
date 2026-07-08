# FIR Digital Filter Design

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![SciPy](https://img.shields.io/badge/SciPy-Signal_Processing-lightblue.svg)](https://scipy.org/)

## Project Description
This repository contains the code, simulations, and academic report for a Digital Signal Processing (DSP) project. The study focuses on the design of low-pass FIR (Finite Impulse Response) filters. 

It mathematically analyzes the ideal brick-wall filter, the Gibbs Phenomenon caused by truncating the impulse response (IRT method), and how windowing techniques offer practical solutions for real hardware implementations, with a special focus on the versatility of the Kaiser window.

## Repository Contents

* `FIR_Filter_Design_Simulations.ipynb`: Jupyter Notebook containing all interactive Python simulations. It generates plots and frequency responses using `scipy.signal`. Features include:
  * Time-domain digital filtering of a signal with high-frequency noise.
  * Comparison between ideal and actual frequency responses.
  * Analysis of the Gibbs Phenomenon evolution across different filter lengths ($N$).
  * Effect of adjusting the $\beta$ parameter in Kaiser window filter design.
* `FIR_Filter_Design_Report_Jorge_Crespo_def.pdf`: Detailed academic report structured in LaTeX covering the theoretical foundations, mathematical derivation, evaluation of standard windows (Rectangular, Hanning, Hamming, Blackman), and final conclusions.

## Requirements & Dependencies

To run the simulations locally, you need Python 3 and the following libraries installed:

```bash
pip install numpy scipy matplotlib jupyterlab
```

## How to Use This Repository

1. Clone this repository to your local machine:
   ```bash
   git clone [https://github.com/jorcreri/FIR-Filter-Design] (https://github.com/jorcreri/FIR-Filter-Design)
   ```
2. Navigate to the project directory:
   ```bash
   cd repo-name
   ```
3. Start Jupyter Notebook or JupyterLab:
   ```bash
   jupyter notebook
   ```
4. Open the `FIR_Filter_Design_Simulations.ipynb` file and run the cells to view the simulations and reproduce the report's plots.

## Key Findings & Conclusions

* **Gibbs Phenomenon:** Direct truncation of the ideal impulse response generates persistent overshoots (approx. 8.95%) in the passband. Increasing the filter order ($N$) does not eliminate the amplitude of these oscillations; it only concentrates them closer to the cut-off frequency.
* **Standard Window Trade-off:** Classic windows successfully smooth out ripples but impose a strict trade-off: a narrower transition band (sharper cut-off) results in lower ripple attenuation, and vice versa.
* **The Kaiser Window:** Provides the most robust solution for practical FIR filter design. Its adjustable parameter ($\beta$) allows DSP designers to mathematically tune and independently balance the transition bandwidth and stop-band attenuation, adapting to specific hardware constraints.

## Author

**Jorge Crespo Rivas** 
University of Thessaly - May 2026

## License

This project is distributed under the MIT License. You are free to use, modify, and distribute this code and documentation for academic or personal purposes.
