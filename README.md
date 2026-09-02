# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
 pip install matplotlib
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import pandas as pd

data = {
    'Month': ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
    'Laptop': [120, 135, 150, 145, 170, 180, 190, 175, 200, 220, 250, 280],
    'Mobile': [200, 220, 210, 240, 260, 270, 290, 300, 310, 330, 350, 380],
    'Tablet': [80, 90, 100, 95, 110, 120, 130, 125, 140, 150, 160, 180],
    'Accessories': [150, 160, 170, 180, 190, 200, 210, 220, 230, 240, 260, 280]
}

df = pd.DataFrame(data)
plt.plot(df['Month'], df['Laptop'])
plt.title('Monthly Laptop Sales')
plt.xlabel('Month')
plt.ylabel('Number of Units Sold')
plt.show()
plt.plot(df['Month'], df['Laptop'], marker='o', label='Laptop')
plt.plot(df['Month'], df['Mobile'], marker='o', label='Mobile')
plt.title('Monthly Product Sales')
plt.xlabel('Month')
plt.ylabel('Units Sold')
plt.legend()
plt.grid()
plt.show()
x = [1, 2, 3]
y = [2, 4, 1]
plt.plot(x, y)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('My first graph!')
plt.show()
x1 = [1, 2, 3]
y1 = [2, 4, 1]
plt.plot(x1, y1, label="line 1")

x2 = [1, 2, 3]
y2 = [4, 1, 3]
plt.plot(x2, y2, label="line 2")

plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('Two lines on same graph!')
plt.legend()
plt.show()
x = [1, 2, 3, 4, 5, 6]
y = [2, 4, 1, 5, 2, 6]

plt.plot(x, y, color='green', linestyle='dashed', linewidth=3,
         marker='o', markerfacecolor='blue', markersize=12)
plt.ylim(1, 8)
plt.xlim(1, 8)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('Some cool customizations!')
plt.show()

years = [2010, 2011, 2012, 2013, 2014, 2015]
yield_apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931]
plt.plot(years, yield_apples)
plt.show()


years = range(2000, 2012)
apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896]

plt.figure(figsize=(12, 6))
plt.plot(years, apples, marker='o')
plt.plot(years, oranges, marker='x')
plt.xlabel('Year')
plt.ylabel('Yield (tons per hectare)')
plt.title("Crop Yields in Kanto")
plt.legend(['Apples', 'Oranges'])
plt.show()
product_sales = {
    'Laptop': df['Laptop'].sum(),
    'Mobile': df['Mobile'].sum(),
    'Tablet': df['Tablet'].sum(),
    'Accessories': df['Accessories'].sum()
}
products = list(product_sales.keys())
sales = list(product_sales.values())
colors = ['skyblue', 'yellow', 'lightgreen', 'pink']

plt.bar(products, sales, color=colors)
plt.title('Total Sales by Product')
plt.xlabel('Product')
plt.ylabel('Total Units Sold')
plt.show()
colors = ['green', 'red', 'blue', 'yellow']
plt.barh(products, sales, color=colors)
plt.title('Total Sales by Product')
plt.xlabel('Total Units Sold')
plt.ylabel('Product')
plt.show()
plt.bar(df['Month'], df['Laptop'], label='Laptop')
plt.bar(df['Month'], df['Mobile'], bottom=df['Laptop'], label='Mobile')
plt.title('Monthly Sales by Product')
plt.xlabel('Month')
plt.ylabel('Units Sold')
plt.legend()
plt.show()
x = [2, 8, 10]
y = [11, 16, 9]
x2 = [3, 9, 11]
y2 = [6, 15, 7]

plt.bar(x, y, color='r')
plt.bar(x2, y2, color='g')
plt.title('Bar graph')
plt.ylabel('Y axis')
plt.xlabel('X axis')
plt.show()
plt.fill_between(df['Month'], df['Laptop'], alpha=0.5, color="red")
plt.title('Laptop Sales Trend')
plt.xlabel('Month')
plt.ylabel('Units Sold')
plt.show()
plt.stackplot(
    df['Month'],
    df['Laptop'],
    df['Mobile'],
    df['Tablet'],
    df['Accessories'],
    labels=['Laptop', 'Mobile', 'Tablet', 'Accessories']
)
plt.title('Monthly Product Sales')
plt.xlabel('Month')
plt.ylabel('Units Sold')
plt.legend(loc='upper left')
plt.show()
x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5, 7, 9, 11, 13]
y3 = [2, 4, 6, 8, 10]

plt.plot(x, y1, color='red')
plt.plot(x, y2, color='black')
plt.fill_between(x, y1, color='blue')
plt.fill_between(x, y2, color='green')
plt.legend(['y1', 'y2'])
plt.show()


plt.stackplot(x, y1, y2, y3, labels=['Line 1', 'Line 2', 'Line 3'])
plt.legend(loc='upper left')
plt.title('Stacked Line Chart')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()

order_sales = [10, 12, 15, 18, 20, 22, 25, 28, 30, 32, 35, 35, 38, 40, 42, 45, 48, 50, 52, 55, 60, 65, 70, 75, 80, 85, 90, 100]
plt.hist(order_sales, bins=8)
plt.title('Distribution of Order Sales')
plt.xlabel('Units per Order')
plt.ylabel('Frequency')
plt.show()

order_sales = [10, 12, 15, 18, 20, 22, 25, 28, 30, 32, 35, 35, 38, 40, 42, 45, 48, 50, 52, 55, 60, 65, 70, 75, 80, 85, 90, 100]
plt.hist(order_sales, bins=8)
plt.title('Distribution of Order Sales')
plt.xlabel('Units per Order')
plt.ylabel('Frequency')
plt.show()
order_sales = [10, 12, 15, 18, 20, 22, 25, 28, 30, 32, 35, 35, 38, 40, 42, 45, 48, 50, 52, 55, 60, 65, 70, 75, 80, 85, 90, 100]
plt.hist(order_sales, bins=8)
plt.title('Distribution of Order Sales')
plt.xlabel('Units per Order')
plt.ylabel('Frequency')
plt.show()

plt.hist(df['Laptop'], bins=5, alpha=0.5, label='Laptop')
plt.hist(df['Mobile'], bins=5, alpha=0.5, label='Mobile')
plt.hist(df['Tablet'], bins=5, alpha=0.5, label='Tablet')
plt.title('Distribution of Product Sales')
plt.xlabel('Units Sold')
plt.ylabel('Frequency')
plt.legend()
plt.show()

ages = [2, 5, 70, 40, 30, 45, 50, 45, 43, 44, 60, 7, 13, 57, 18, 90, 77, 32, 21, 20, 40]
plt.hist(ages, bins=10, range=(0, 100), color='green', histtype='bar', rwidth=0.8)
plt.xlabel('age')
plt.ylabel('No. of people')
plt.title('My histogram')
plt.show()
plt.pie(sales, labels=products, autopct='%1.1f%%')
plt.title('Product Sales Distribution')
plt.show()
data = {
    'Product': ['Laptop', 'Mobile', 'Tablet', 'Accessories'],
    'Sales': [280, 380, 180, 280]
}
df = pd.DataFrame(data)

explode = [0, 0.1, 0, 0]
colors = ['gold', 'skyblue', 'lightgreen', 'orange']

plt.pie(
    df['Sales'],
    labels=df['Product'],
    colors=colors,
    autopct='%1.1f%%',
    explode=explode,
    startangle=90,
    shadow=True,
    textprops={'fontsize': 11},
    wedgeprops={'width': 0.8}
)
plt.title('Product Sales Distribution')
plt.axis('equal')
plt.show()
activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']

plt.pie(
    slices,
    labels=activities,
    colors=colors,
    startangle=90,
    shadow=True,
    explode=(0, 0, 0.1, 0),
    radius=1.2,
    autopct='%1.1f%%'
)
plt.legend()
plt.show()
sales = [120, 135, 150, 145, 170, 180, 190, 175, 200, 220, 250, 280, 310, 125, 140, 155, 165, 185, 600]

# Standard
plt.boxplot(sales)
plt.title('Sales Distribution with Outlier')
plt.ylabel('Sales')
plt.show()


plt.boxplot(sales, showmeans=True)
plt.title('Sales Distribution')
plt.ylabel('Sales')
plt.show()
laptop = [120, 135, 150, 145, 170, 180, 190, 175, 200]
mobile = [200, 220, 210, 240, 260, 270, 290, 300, 310]
tablet = [80, 90, 100, 95, 110, 120, 130, 125, 140]

plt.boxplot([laptop, mobile, tablet], labels=['Laptop', 'Mobile', 'Tablet'])
plt.title('Sales Distribution by Product')
plt.xlabel('Product')
plt.ylabel('Units Sold')
plt.show()

plt.boxplot([laptop, mobile, tablet], labels=['Laptop', 'Mobile', 'Tablet'], vert=False)
plt.title('Sales Distribution by Product')
plt.xlabel('Units Sold')
plt.show()
plt.scatter(df['Laptop'], df['Mobile'])
for i in range(len(df)):
    plt.annotate(df['Month'][i], (df['Laptop'][i], df['Mobile'][i]))
plt.title('Laptop Sales vs Mobile Sales')
plt.xlabel('Laptop Sales')
plt.ylabel('Mobile Sales')
plt.show()
plt.scatter(df['Month'], df['Laptop'], color='blue', s=100, label='Laptop')
plt.scatter(df['Month'], df['Mobile'], color='red', s=100, label='Mobile')
plt.xlabel('Month')
plt.ylabel('Sales')
plt.title('Laptop vs Mobile Monthly Sales')
plt.legend()
plt.grid(True)
plt.show()
fig, ax = plt.subplots(2, 2, figsize=(12, 8))

ax[0, 0].plot(df['Month'], df['Laptop'])
ax[0, 0].set_title('Laptop Sales')

ax[0, 1].bar(products, sales)
ax[0, 1].set_title('Total Product Sales')

ax[1, 0].hist(order_sales, bins=8)
ax[1, 0].set_title('Order Distribution')

advertising_costs = [50, 70, 90, 110, 130, 150, 170, 190, 210, 230, 250, 270]
sales_from_advertising = [100, 150, 180, 220, 250, 280, 300, 330, 350, 380, 400, 420]
ax[1, 1].scatter(advertising_costs, sales_from_advertising)
ax[1, 1].set_title('Advertising vs Sales')
ax[1, 1].set_xlabel('Advertising Costs')
ax[1, 1].set_ylabel('Sales From Advertising')

plt.tight_layout()
plt.show()
x = np.arange(0, 4 * np.pi, 0.1)
y = np.sin(x)

plt.plot(x, y)
plt.title("sine wave form")
plt.show()
from scipy.interpolate import make_interp_spline

x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])

spl = make_interp_spline(x, y)
x_smooth = np.linspace(x.min(), x.max(), 100)
y_smooth = spl(x_smooth)

plt.plot(x, y, 'o', label='data')
plt.plot(x_smooth, y_smooth, '-', label='spline')
plt.legend()
plt.show()
# Simple line from points
x_values = [0, 1, 2, 3, 4, 5]
y_values = [0, 1, 4, 9, 16, 25]
plt.plot(x_values, y_values)
plt.show()


x = np.arange(0, 10)
y = x * x
plt.plot(x, y, 'g*', linestyle='dashed', linewidth=2, markersize=12)
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.title('2d Diagram')
plt.show()


x_values = [0, 1, 2, 3, 4, 5]
y_values = [0, 1, 4, 9, 16, 25]
plt.plot(x_values, y_values)
plt.show()


x = np.arange(0, 10)
y = x * x
plt.plot(x, y, 'g*', linestyle='dashed', linewidth=2, markersize=12)
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.title('2d Diagram')
plt.show()
# Colored scatter plot with savefig
x = np.arange(0, 10)
y = np.arange(11, 21)
plt.scatter(x, y, c='r')
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.title('Graph in 2D')
plt.savefig('Test.png')


x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
y = [2, 4, 5, 7, 6, 8, 9, 11, 12, 12]
plt.scatter(x, y, label="stars", color="green", marker="*", s=30)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('My scatter plot!')
plt.legend()
plt.show()
values = [5, 6, 3, 7, 2]
names = ["A", "B", "C", "D", "E"]


plt.bar(names, values, color="green")
plt.show()


plt.barh(names, values, color="yellowgreen")
plt.show()
x = [2, 1, 6, 4, 2, 4, 8, 9, 4, 2, 4, 10, 6, 4, 5, 7, 7, 3, 2, 7, 5, 3, 5, 9, 2, 1]
plt.hist(x, bins=10, color='blue', alpha=0.5)
plt.show()
np.random.seed(0)
data = np.random.normal(loc=0, scale=1, size=100)

fig, ax = plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Values')
ax.set_title('Box Plot')
plt.show()
labels = 'Python', 'C++', 'Ruby', 'Java'
sizes = [215, 130, 245, 210]
colors = ['gold', 'yellowgreen', 'lightcoral', 'lightskyblue']
explode = (0, 0.4, 0, 0.5)

plt.pie(sizes, explode=explode, labels=labels, colors=colors, autopct='%1.1f%%', shadow=True)
plt.axis('equal')
plt.show()
x = np.arange(0, 10)
y = x * x

plt.subplot(2, 2, 1)
plt.plot(x, y, "r--")

plt.subplot(2, 2, 2)
plt.plot(x, y, "g*--")

plt.subplot(2, 2, 3)
plt.plot(x, y, 'bo')

plt.subplot(2, 2, 4)
plt.plot(x, y, 'go')

plt.show()
```

# Result:
<img width="573" height="457" alt="image" src="https://github.com/user-attachments/assets/1ba74d93-b9fc-43d3-9de0-9efd8f5047a7" />
<img width="609" height="481" alt="image" src="https://github.com/user-attachments/assets/4d59c6b7-0532-42bf-8c0f-02460d7ddaee" />
<img width="590" height="478" alt="image" src="https://github.com/user-attachments/assets/b6780085-2ed4-404f-93d7-0afa017239ec" />
<img width="566" height="457" alt="image" src="https://github.com/user-attachments/assets/16249511-9dfb-4a99-ba64-4c48a0d5f431" />
<img width="562" height="457" alt="image" src="https://github.com/user-attachments/assets/d65fbb14-2002-4491-831c-b32b3642578b" />
<img width="565" height="413" alt="image" src="https://github.com/user-attachments/assets/635d34f5-344a-4d26-83de-6759f5655fc2" />
<img width="1010" height="547" alt="image" src="https://github.com/user-attachments/assets/f99bc9c3-04de-48ea-8956-7862bb27eaa8" />
<img width="580" height="455" alt="image" src="https://github.com/user-attachments/assets/82b53fb7-11ef-4590-8709-734c22c0096f" />
<img width="639" height="455" alt="image" src="https://github.com/user-attachments/assets/b7e44ea1-30c3-4e6c-a016-ede08bd9e0a5" />
<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/169ae1a4-1e4a-466d-99ec-5927e51cafec" />
<img width="563" height="455" alt="image" src="https://github.com/user-attachments/assets/b1f55225-55e9-4ab2-89b9-f8b46ed3b92e" />
<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/5a780bf8-aa3b-4eaf-814b-466c57331d72" />
<img width="580" height="455" alt="image" src="https://github.com/user-attachments/assets/7120babb-0973-4b93-aa96-77f1f0145f46" />
<img width="556" height="413" alt="image" src="https://github.com/user-attachments/assets/6156a5eb-de6c-46b7-bbe2-ba488ed1493a" />
<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/ecd0a992-b58d-4bea-97c4-80d5a93c4149" />
<img width="554" height="455" alt="image" src="https://github.com/user-attachments/assets/2b10fe5b-3f9b-4aaf-acdb-61b341e64206" />
<img width="567" height="455" alt="image" src="https://github.com/user-attachments/assets/4713a34e-78e3-4b65-b180-200c86dff917" />
<img width="396" height="411" alt="image" src="https://github.com/user-attachments/assets/bb3b6dba-09b9-4d89-bfac-1609e8b9b706" />
<img width="515" height="411" alt="image" src="https://github.com/user-attachments/assets/160bca6c-c219-4582-9e5f-c6473df2f29b" />
<img width="435" height="401" alt="image" src="https://github.com/user-attachments/assets/ce364719-a246-49fc-9734-0325275d878a" />
<img width="571" height="435" alt="image" src="https://github.com/user-attachments/assets/1600dcff-2e90-4d3d-8d70-7ea29cd18797" />
<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/edf16078-4f4a-46ed-98f2-768c373b1ff2" />
<img width="573" height="455" alt="image" src="https://github.com/user-attachments/assets/a7d8ef36-86f1-4a7d-90dc-af7f13d3932a" />
<img width="575" height="455" alt="image" src="https://github.com/user-attachments/assets/91f94cb6-f820-4ec4-adbb-3a75689384e7" />
<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/925e7bab-5ae5-4122-9d3f-46f862069d9a" />
<img width="1189" height="790" alt="image" src="https://github.com/user-attachments/assets/b699b10a-f493-4f23-a94f-056a7e2dc49b" />
<img width="568" height="435" alt="image" src="https://github.com/user-attachments/assets/26f9f438-add4-430b-8299-7fbc36c037dc" />
<img width="543" height="413" alt="image" src="https://github.com/user-attachments/assets/7ab84da0-e861-4949-965a-d23de87b22e7" />
<img width="543" height="413" alt="image" src="https://github.com/user-attachments/assets/9bde59b1-f42c-4542-b0aa-6d0da28de441" />
<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/3e81c437-d635-4cdf-9b67-ba408e9baa01" />
<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/21ccd654-3666-4cc6-b091-545a64e08719" />
<img width="534" height="413" alt="image" src="https://github.com/user-attachments/assets/2e737529-8e12-4059-8309-d4627a37d733" />
<img width="536" height="413" alt="image" src="https://github.com/user-attachments/assets/81f8b46b-03fd-4c13-b8d9-92f1ec5f118a" />
<img width="534" height="413" alt="image" src="https://github.com/user-attachments/assets/54ad51f5-1d72-4deb-97f6-3166f9d20ec0" />
<img width="565" height="455" alt="image" src="https://github.com/user-attachments/assets/90ce9061-fb0d-4d8e-be9c-0ab058376a29" />
<img width="515" height="389" alt="image" src="https://github.com/user-attachments/assets/dd14ed86-3355-4823-b6bb-acf93bfb637f" />
<img width="543" height="413" alt="image" src="https://github.com/user-attachments/assets/99f50afb-2728-4ab8-bf02-8965cea39ab0" />


 
