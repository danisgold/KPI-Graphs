# KPI-Graphs
KPI Graphs for Ben


def print_hi(name):
    # Use a breakpoint in the code line below to debug your script.
    print(f'Hi, {"Carpe"}')  # Press ⌘F8 to toggle the breakpoint.


# Press the green button in the gutter to run the script.
if __name__ == '__main__':
    print_hi('PyCharm')

# See PyCharm help at https://www.jetbrains.com/help/pycharm/

#Key Data Asset and Evaluation Metrics

import numpy as np
import matplotlib.pyplot as plt


# data to plot
n_groups = 4
means_Q1 = (70,19,6,3)
means_Q2 = (10,18,23,5)

# create plot
fig, ax = plt.subplots()
index = np.arange(n_groups)
bar_width = 0.25
opacity = 0.8

rects1 = plt.bar(index, means_Q1, bar_width,
alpha=opacity,
color='b',
label='Q1')

rects2 = plt.bar(index + bar_width, means_Q2, bar_width,
alpha=opacity,
color='r',
label='Q2')

plt.xlabel('')
plt.ylabel('')
plt.title('Data Asset and Evaluation Key Metrics')
plt.xticks(index + bar_width, ('Active Datasets', 'Active Providers', 'Evaluations in Progress', 'Evaluations Completed'))
plt.legend()

plt.tight_layout()
plt.show()

#Percent of Budget Spent
y = np.array([94.26, 5.74])
mylabels = ["Percent of Budget Spent (94.26%)", "Remainder (5.74%)"]
myexplode = [0, 0.2]
plt.title('Percent of Budget Spent')
plt.pie(y, labels=mylabels, explode=myexplode)
plt.show()

#Percentage of Time Spent on Open and Completed Evals


# creating the dataset
y = np.array([33, 67])
mylabels = ["Percent of Time Spent on Evaluations (33%)", "Other (67%)"]
myexplode = [0, 0.1]
plt.title('Percentage of Time Spent on Open and Completed Q1 Evaluations')
plt.pie(y, labels=mylabels, explode=myexplode)
plt.show()

y = np.array([51, 49])
mylabels = ["Percent of Time Spent (51%)", "Other (49%)"]
myexplode = [0, 0.1]
plt.title('Percentage of Time Spent on Open and Completed Q2 Evaluations')
plt.pie(y, labels=mylabels, explode=myexplode)
plt.show()


#Days Spent on Open and Completed Evals
ndata = {'': 100, 'End of Q1': 18, 'End of Q2': 56, '': 100,}
Q = ['', 'End of Q1', 'End of Q2', ' ']
values = [99, 18, 56, 99]
w = [0.01, 0.8, 0.8, 0.001]
# creating the bar plot
plt.bar(Q, values, color=['white', 'red', 'blue', 'white'],
        width=w)


plt.title("Days Spent on Open and Completed Evaluations")
plt.show()
