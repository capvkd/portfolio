# Hourly Schedule Optimization

## Problem Statement

We are given data by a company that employs drivers to make deliveries by car. Employees are scheduled and paid a fixed amount per hour, regardless of the number of deliveries completed. We have been provided with data on both order volume and driver performance (deliveries/hour) for a market. In this project, we develop a weekly schedule that ensures deliveries are made on-time while minimizing payroll costs. 

### Assumptions
1.	A driver is paid $10/hour at all times.
2.	Driver shifts must be either 5, 6, 7, or 8 hours in length.
3.	Do not account for breaks in work.
4.	Driver performance data assumes peak deliveries per hour with on-time delivery.
5.	Assume orders arrive in regular cadence during the time intervals shown.

### Spreadsheet Tabs
1. `Information`: project description and instructions for using the schedule optimization tool.
2. `Market Order Volume`: Number of order for the week of 5/20/19, broken down by half-hour intervals.
3. `Market Driver Data`: Weekly average driver performance (deliveries completed per hour), broken down by half-hour intervals.
4. `Schedule`: The schedule optimizer, which takes the data from tabs 2 and 3, plus schedule inputs from the user to determine the best schedule at minimal cost.

The completed product outlines the shifts for each day, their length, and total daily/weekly labor cost. The solution structure is easily adaptable for weekly use by replacing the order volume forecast in tab 2.

## Solution

### Tool Description

This excel tool takes order volume and driver performance data to determine the minimum amount drivers needed during half-hour intervals. Then, using this data, and input in the form of shift start and end times, the tool will solve for the number of drivers to assign to each shift while solving for the lowest daily cost.

To accomplish this, we make use of Excel's Solver feature to create a constraint problem. We also create macros to automate the running of the contraint problems, which initiate upon the user clicking a button.

### Problem Constraints

1. The delivery capacity (`Schedule I26:O59`) for each half-hour interval has to meet or exceed the expected demand (`Market Order Volume`, `Schedule P26:V59`).
2. The daily cost (`Schedule A16:B24`) should be positive and as close to 0 as possible.

### Tool Instructions

1. Add updated order volume data to `Market Order Volume Data` (if newer data available).
2. Add updated driver performance data to `Market Driver Data` (if newer data available).
3. Switch to the `Schedule` tab, and select start times and end times for daily shifts (rows 3-13).
4. For each day, click the `Schedule` button to optimize the daily shifts (rows 14-15).

### Tool Outputs
After following the steps above, the tool outputs the following in the `Schedule` tab:
 - A16:B24 shows the daily and weekly labor costs.
 - Columns D2:D13, H2:H13, L2:L13, P2:P13, T2:T13, X2:X13, and AB2:AB13 display the number of employees needed for each shift on the given day.
