# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

## Date: 20/05/2026
## Roll.No: 212225040323

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding:

```
DevelopedBy: K RAGAPRIYAN
RegNo: 212225040323
import matplotlib.pyplot as plt
import numpy as np

# ---------------- LINE PLOT 1 ----------------
x_values = [0, 1, 2, 3, 4, 5]
y_values = [0, 1, 4, 9, 16, 25]

plt.plot(x_values, y_values)
plt.title("Simple Line Plot")
plt.show()

# ---------------- LINE PLOT 2 ----------------
x = [1, 2, 3]
y = [2, 4, 1]

plt.plot(x, y)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('My first graph!')
plt.show()

# ---------------- TWO LINES ----------------
x1 = [1, 2, 3]
y1 = [2, 4, 1]

x2 = [1, 2, 3]
y2 = [4, 1, 3]

plt.plot(x1, y1, label="line 1")
plt.plot(x2, y2, label="line 2")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Two lines on same graph!')
plt.legend()
plt.show()

# ---------------- CUSTOM LINE ----------------
x = [1, 2, 3, 4, 5, 6]
y = [2, 4, 1, 5, 2, 6]

plt.plot(
    x, y,
    color='green',
    linestyle='dashed',
    linewidth=3,
    marker='o',
    markerfacecolor='blue',
    markersize=12
)

plt.ylim(1, 8)
plt.xlim(1, 8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Some cool customizations!')
plt.show()

# ---------------- APPLE YIELD ----------------
yield_apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931]
plt.plot(yield_apples)
plt.title("Apple Yield")
plt.show()

years = [2010, 2011, 2012, 2013, 2014, 2015]
yield_apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931]

plt.plot(years, yield_apples)
plt.title("Apple Yield over Years")
plt.show()

# ---------------- APPLES & ORANGES ----------------
years = list(range(2000, 2012))

apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931,
          0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]

oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908,
           0.907, 0.904, 0.901, 0.898, 0.900, 0.896]

plt.plot(years, apples, label="Apples")
plt.plot(years, oranges, label="Oranges")

plt.xlabel('Year')
plt.ylabel('Yield (tons per hectare)')
plt.title("Crop Yields in Kanto")
plt.legend()
plt.show()

# ---------------- FIGURE SIZE ----------------
plt.figure(figsize=(12, 6))
plt.plot(years, oranges, marker='o')
plt.title("Yield of Oranges")
plt.show()

# ---------------- SCATTER PLOT ----------------
x_values = [0, 1, 2, 3, 4, 5]
y_values = [0, 1, 4, 9, 16, 25]

plt.scatter(x_values, y_values, s=30, color="blue")
plt.title("Scatter Plot")
plt.show()

# ---------------- SINE WAVE ----------------
x = np.arange(0, 4 * np.pi, 0.1)
y = np.sin(x)

plt.plot(x, y)
plt.title("Sine Wave")
plt.show()

# ---------------- STACK / FILL ----------------
x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5, 7, 9, 11, 13]

plt.fill_between(x, y1, color="blue", alpha=0.5)
plt.fill_between(x, y2, color="green", alpha=0.5)

plt.plot(x, y1, color="red")
plt.plot(x, y2, color="black")

plt.legend(['y1', 'y2'])
plt.title("Fill Between Plot")
plt.show()

# ---------------- BAR GRAPH ----------------
names = ['one', 'two', 'three', 'four', 'five']
height = [10, 24, 36, 40, 5]

plt.bar(names, height, width=0.8, color='green')
plt.title('Bar Chart')
plt.show()

# ---------------- MULTIPLE BAR ----------------
x = [2, 8, 10]
y = [11, 16, 9]

x2 = [3, 9, 11]
y2 = [6, 15, 11]

plt.bar(x, y, color='r')
plt.bar(x2, y2, color='g')

plt.title('Bar Graph')
plt.show()

# ---------------- HISTOGRAM ----------------
ages = [2, 5, 70, 40, 30, 45, 50, 45, 50, 45,
        43, 40, 44, 60, 7, 13, 57, 18, 90, 77,
        32, 21, 20, 40]

plt.hist(ages, bins=10, range=(0, 100),
         color='green', histtype='bar', rwidth=0.8)

plt.title('Histogram')
plt.show()

# ---------------- BOX PLOT (FIXED ERROR) ----------------
np.random.seed(0)
data = np.random.normal(loc=0, scale=1, size=100)

fig, ax = plt.subplots()
ax.boxplot(data)

ax.set_xlabel('Data')
ax.set_ylabel('Values')
ax.set_title('Box Plot')

plt.show()

# ---------------- PIE CHART 1 ----------------
labels = ['Python', 'C++', 'Ruby', 'Java']
sizes = [215, 130, 245, 210]
colors = ['gold', 'yellowgreen', 'lightcoral', 'lightskyblue']
explode = (0, 0.4, 0, 0.5)

plt.pie(sizes, labels=labels, colors=colors,
        explode=explode, autopct='%1.1f%%',
        shadow=True)

plt.axis('equal')
plt.show()

# ---------------- PIE CHART 2 ----------------
activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']

plt.pie(slices, labels=activities, colors=colors,
        startangle=90, shadow=True,
        explode=(0, 0, 0.1, 0),
        radius=1.2, autopct='%1.1f%%')

plt.legend()
plt.show()
```

# Output:

![alt text](<Screenshot 2026-06-08 233149.png>)
![alt text](<Screenshot 2026-06-08 233206.png>)
![alt text](<Screenshot 2026-06-08 233222.png>)
![alt text](<Screenshot 2026-06-08 233238.png>)
![alt text](<Screenshot 2026-06-08 233307.png>)
![alt text](<Screenshot 2026-06-08 233322.png>)
![alt text](<Screenshot 2026-06-08 233340.png>)
![alt text](<Screenshot 2026-06-08 233355.png>)
![alt text](<Screenshot 2026-06-08 233409.png>)
![alt text](<Screenshot 2026-06-08 233422.png>)
![alt text](<Screenshot 2026-06-08 233435.png>)
![alt text](<Screenshot 2026-06-08 233451.png>) 
![alt text](<Screenshot 2026-06-08 233503.png>)
![alt text](<Screenshot 2026-06-08 233517.png>)
![alt text](<Screenshot 2026-06-08 233532.png>)
![alt text](<Screenshot 2026-06-08 233546.png>)
![alt text](<Screenshot 2026-06-08 233559.png>)

# Result:

Thus, data visualization using the Matplotlib library was successfully performed. Different graphs such as line plot, bar chart, scatter plot, histogram, pie chart, and box plot were generated to represent and analyze the given data effectively.