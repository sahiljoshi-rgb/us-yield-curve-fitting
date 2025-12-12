# Term Structure of US Treasury Yield Volatility and Curve Fitting  
### Nelson-Siegel and Cubic Splines

This repository contains a research-style Jupyter notebook analyzing the **US Treasury yield curve**, focusing on:

- Volatility behavior across maturities  
- Parametric curve fitting using the **Nelson-Siegel model**  
- Non-parametric curve fitting using **manually constructed cubic splines**

---

## Data

- **Source:** Federal Reserve Economic Data (FRED)
- **Instruments:** US Treasury yields (1M-30Y)
- **Frequency:** Daily
- **Sample:** 1975-2025 (subsettable to post-1990)

---

## Methodology

1. **Volatility Analysis**  - Cross-maturity comparison of yield dispersion to understand term-structure risk.

2. **Nelson-Siegel Fitting**  
   - Level, slope, curvature factor interpretation  
   - Comparison across economic regimes (pre-COVID vs pre-GFC flattening)

3. **Cubic Spline Fitting**  
   - Manual spline construction using linear algebra  
   - Smooth interpolation without imposing factor structure

---

## Key Takeaways

- Short-term yields exhibit higher volatility due to policy sensitivity.
- Nelson–Siegel provides a compact, interpretable representation but struggles with inverted/flattened curves.
- Cubic splines offer flexibility at the cost of economic interpretability.

---

## Visuals

### Standard Deviations of Treasury Yields by Maturity
<img width="695" height="473" alt="image" src="https://github.com/user-attachments/assets/b85ce8f8-9046-4c29-8d7f-00aa3ef2b451" />

### Nelson-Siegel Fit to Treasury Yield Curve (1)
<img width="850" height="550" alt="image" src="https://github.com/user-attachments/assets/3257504b-6ac5-4ef5-ba5a-da9e344240ce" />

###  Nelson-Siegel Fit to Treasury Yield Curve (2)
<img width="858" height="550" alt="image" src="https://github.com/user-attachments/assets/7493c1ed-d203-4a4b-b8a7-9aff41ab39ab" />

### Cubic-Spline Fit to Treasury Yield Curve (2)
<img width="850" height="550" alt="image" src="https://github.com/user-attachments/assets/0b1e4411-df36-4288-a1bd-58749182f941" />

---

## How to Run

```bash
pip install -r requirements.txt
```

### 1. Install Dependencies
``` pip install -r requirements.txt ```

### 2. Launch Jupyter Notebook
``` jupyter notebook notebooks/us-yield-curve-fitting.ipynb ```

### 3. Requirements
```
- pandas
- numpy
- matplotlib
- seaborn
- fredapi
- nelson-siegel-svensson
```

### 4. You will need a free FRED API key:
``` https://fred.stlouisfed.org/docs/api/api_key.html ```

### 5. Data Source Attribution
``` All data is sourced from: FRED (Federal Reserve Economic Data) ```

### 6. Yield series used: 
``` DGS1MO, DGS3MO, DGS6MO, DGS1, DGS2, DGS3, DGS5, DGS7, DGS10, DGS20, DGS30 ```

### 7. License
``` This project is licensed under the MIT License. ```

### 8. Author
Sahil Joshi (LinkedIn: https://www.linkedin.com/in/sahil-joshi-90338a212/)

### 11. References
- This project was developed with guidance from the yield-curve and term-structure coursework in the **WorldQuant University MSc in Financial Engineering** program.
