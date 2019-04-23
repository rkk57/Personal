

```python
from aguaclara.core.units import unit_registry as u
import aguaclara.research.environmental_processes_analysis as epa
import aguaclara.core.physchem as pc
import aguaclara.core.utility as ut
import aguaclara.research.procoda_parser as pp

import numpy as np
import matplotlib.pyplot as plt
import collections
import os
from pathlib import Path
import pandas as pd
import statistics


filename="https://raw.githubusercontent.com/AguaClara/Dissolved-Gas/master/Data/TestingTemperatureDifference_Trial01_20190319.xls"

data=pd.read_csv(filename, delimiter="\t")

data=pp.remove_notes(data)

Time=data["Day fraction since midnight on "]
Temp=data['Temperature In (C)']
Time=pd.to_numeric(Time)

plt.plot(Time,Temp)
plt.show()





```
