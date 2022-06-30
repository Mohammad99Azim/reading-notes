# Pyplot

``matplotlib.pyplot`` is a collection of functions that make matplotlib work like MATLAB. Each pyplot function makes some change to a figure: creates a figure, creates a plotting area in a figure, plots some lines in a plotting area, decorates the plot with labels, etc.





1- creates a plotting


```
import matplotlib.pyplot as plt
plt.plot([1, 2, 3, 4], [1, 4, 9, 16])plt.ylabel('some numbers')
plt.show()
```
Output:

![Output](https://matplotlib.org/stable/_images/sphx_glr_pyplot_002.png)

**Note!!!**

For every x, y pair of arguments, there is an optional third argument which is the format string that indicates the color and line type of the plot. The letters and symbols of the format string are from MATLAB, and you concatenate a color string with a line style string. The default format string is 'b-', which is a solid blue line. For example, to plot the above with red circles, you would issue
```
plt.plot([1, 2, 3, 4], [1, 4, 9, 16], 'ro')
plt.axis([0, 6, 0, 20])
plt.show()
```
Output:

![Output](https://matplotlib.org/stable/_images/sphx_glr_pyplot_003.png)






## Things I want to know more about

i want learn more about the data visualisation and how to choos the correct type based on the data you have

