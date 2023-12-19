## What is the Dataset ?

The above dataset contains x, y, Cp values of 1598 different 2-D cross-sections of airfoils with a panel size of 160. The airfoil co-ordinates for different over 1598 different airfoils were downloaded from the UIUC database, passed through XFoil for repanelling and generating corresponding Cp values. They were then packaged as a parquet file.

## Using the Dataset ?

The above dataset can be used by downloading the parquet file and using pandas to import it as follows :
```python
import pandas as pd
df = pd.read_parquet("<file_location>")
X = df['x'] # contains 1598 tensors of size (160)
Y = df['y'] # contains 1598 tensors of size (160)
CP = df['Cp'] # contains 1598 tensors of size (160)

```