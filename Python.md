# Python

## Graph/curves with Python

Packages: `pandas`, `hvplot`


```python
df = pd.read_csv('IQTBT-5mmI-SO2 0.15 (1).csv')
(
    df.hvplot.line(x='MTF0_X_Axis', y='MTF_X', label='MTF X') *
    # df.hvplot.line(x='MTF0_X_Axis', y='MTF_0_X') *
    df.hvplot.line(x='MTF0_Y_Axis', y='MTF_Y', label='MTF Y') *
    # df.hvplot.line(x='MTF0_X_Axis', y='MTF_0_Y') *
    # df.hvplot.line(x='Frequency (lp/mm)', y='Zemax', label='Zemax (s)') *
    df.hvplot.line(x='Frequency (lp/mm)', y='Experimental', label='Experimental (s)') *
    # df.hvplot.line(x='Frequency (lp/mm).1', y='Zemax.1', label='Zemax (t)') *
    df.hvplot.line(x='Frequency (lp/mm).1', y='Experimental.1', label='Experimental (t)')
)
```
