# Daily Pandas & Matplotlib Practice with ChatGPT, Claude, Meta AI (WhatsApp) 17th November 2026
<b>Dataset for today's revision</b></br>
A fresh environmental monitoring dataset:</br>
```Python
import pandas as pd
import numpy as np

df = pd.DataFrame({
    "site_id": [401, 402, 403, 404, 405, 406, 407, 408],
    "district": [
        "Kolkata", "Howrah", "Patna", "Cuttack",
        "Kolkata", "Patna", "Howrah", "Cuttack"
    ],
    "landuse": [
        "Urban", "Agriculture", "Forest", "Forest",
        "Urban", "Agriculture", "Urban", "Forest"
    ],
    "ndvi": [0.22, 0.58, 0.82, 0.76, np.nan, 0.64, 0.31, 0.91],
    "rainfall": [310, 180, 360, 250, 280, np.nan, 190, 450],
    "elevation": [10, 42, 85, 130, 15, 95, 28, 115]
})
```
<b>Exercise 1 — Warm-up</b></br>
Complete these four tasks:</br>
<b>A.</b> Display the first five rows.</br>
<b>B.</b> Display the DataFrame's number of rows and columns.</br>
<b>C.</b> Display only site_id, district and ndvi.</br>
<b>D.</b> Display the descriptive statistics of numerical columns.</br>
Use the appropriate Pandas methods.</br>
Don't worry about speed. Let's see what you remember without looking at your previous code. 💻</br>

# Solution (Script)
```Python
import pandas as pd
import numpy as np

df = pd.DataFrame({
    "site_id": [401, 402, 403, 404, 405, 406, 407, 408],
    "district": [
        "Kolkata", "Howrah", "Patna", "Cuttack",
        "Kolkata", "Patna", "Howrah", "Cuttack"
    ],
    "landuse": [
        "Urban", "Agriculture", "Forest", "Forest",
        "Urban", "Agriculture", "Urban", "Forest"
    ],
    "ndvi": [0.22, 0.58, 0.82, 0.76, np.nan, 0.64, 0.31, 0.91],
    "rainfall": [310, 180, 360, 250, 280, np.nan, 190, 450],
    "elevation": [10, 42, 85, 130, 15, 95, 28, 115]
})
print(df.head(5))
print(df.shape)
print(df[["site_id", "district", "ndvi"]])
print(df.describe())
```
# Solution (Output)
```
PS C:\Users\hp\Downloads\sql_practice(0)> & 'c:\Users\hp\AppData\Local\Programs\Python\Python313\python.exe' '"c:/Users/hp/Downloads/sql_practice(0)/test2.py"'
   site_id district      landuse  ndvi  rainfall  elevation
0      401  Kolkata        Urban  0.22     310.0         10
1      402   Howrah  Agriculture  0.58     180.0         42
2      403    Patna       Forest  0.82     360.0         85
3      404  Cuttack       Forest  0.76     250.0        130
4      405  Kolkata        Urban   NaN     280.0         15
(8, 6)
   site_id district  ndvi
0      401  Kolkata  0.22
1      402   Howrah  0.58
2      403    Patna  0.82
3      404  Cuttack  0.76
4      405  Kolkata   NaN
5      406    Patna  0.64
6      407   Howrah  0.31
7      408  Cuttack  0.91
         site_id      ndvi    rainfall   elevation
count    8.00000  7.000000    7.000000    8.000000
mean   404.50000  0.605714  288.571429   65.000000
std      2.44949  0.258319   95.468768   46.977198
min    401.00000  0.220000  180.000000   10.000000
25%    402.75000  0.445000  220.000000   24.750000
50%    404.50000  0.640000  280.000000   63.500000
75%    406.25000  0.790000  335.000000  100.000000
max    408.00000  0.910000  450.000000  130.000000
PS C:\Users\hp\Downloads\sql_practice(0)> 
```
