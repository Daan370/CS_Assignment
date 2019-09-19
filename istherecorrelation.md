# The code
```python

import numpy as np
import matplotlib.pyplot as plt


Years = np.linspace(2006, 2018, 13)

fig, ax1 = plt.subplots()

ax2 = ax1.twinx()
ax1.plot(Years, S, 'b-')
ax2.plot(Years, L, 'y-')

plt.title("Correlation of WO students and Alcohol in NL")
ax1.set_xlabel('Year')
ax1.set_ylabel('WO students[*1000]', color='b')
ax2.set_ylabel('Liters of beer consumed in NL', color='y')

fig.savefig('WO vs Beer.png', dpi=300)

plt.show()
```
![alt text](https://github.com/Daan370/plot-wo-vs-beer/blob/master/WO%20vs%20beer%20plot.png "The plot of beer")

```python
%matplotlib inline
import matplotlib.pyplot as plt
import numpy as np

# Year;WO [x1000];NL Beer consumption [x1000 hectoliter]

Y = [2006, 2007, 2008, 2009, 2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018]
S = [205.9, 208.6, 212.7, 220.5, 233.2, 242.4, 245.4, 241.4, 250.2, 255.7, 261.2, 267.9, 280.1]
L = [11402, 11492, 11450, 11502, 11474, 11480, 11452, 11484, 11555, 11601, 11731, 11862, 12048]

#Liters per student = LS
res = [(i / j) for i, j in zip(L, S)] 
print ("The division list is : " + str(res)) 
Years = np.linspace(2005, 2019, 15)

x = [Years]
y = [S]
plt.plot(Y, res, 'ro-') 
plt.title("Average amount of alcohol per student in NL")
plt.xlabel('Year')
plt.ylabel('Liters of beer per student')
leg = plt.legend()

fig.savefig('Amount of beer per student.png', dpi=300)

plt.show()
```
![alt text](https://github.com/Daan370/plot-wo-vs-beer/blob/master/Average%20amount%20of%20beer%20per%20student.png)

