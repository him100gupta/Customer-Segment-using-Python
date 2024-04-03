## Importing libraries

``` Python
import numpy as np
import pandas as pd
import scipy

import matplotlib.pyplot as plt
import seaborn as sns
sns.set()

from sklearn.preprocessing import StandardScaler

from scipy.cluster.hierarchy import dendrogram, linkage
from sklearn.cluster import KMeans
```
## Importing data
``` Python
df = pd.read_csv('customer_segmentation_data.csv', sep = ',', index_col = False)
```
## EDA
``` Python
df.describe()
```
``` Python
## Checking for missing values
df.isnull().sum()
```
``` Python
## copying the data
df_seg = df.copy()
```
``` Python
## Filling missing values
df_seg = df_seg.fillna(0)
```
``` Python
df_seg.head()
```
``` Python
df_seg.dtypes
```
### Correlation
``` Python
df_seg.corr()
```
#### Correlation heat map
``` Python
plt.figure(figsize = (10, 6))
s = sns.heatmap(df_seg.corr(),
               annot = True, 
               cmap = 'RdBu',
               vmin = -1, 
               vmax = 1)
s.set_yticklabels(s.get_yticklabels())
s.set_xticklabels(s.get_xticklabels())
plt.title('Correlation Heatmap', fontsize = 12)
plt.savefig('corr.png')
plt.show()
```

``` Python

```

``` Python

```

``` Python

```
