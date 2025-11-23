** Files Explained **

1) The fileReader class makes a file reader that can read numerical CSV values. What it does is that it creates a paired vector structure so that each index stores <Number, vector<Values>>. This allows us to store the different colums as <column, vector <ColValues>>. 

2) ewmaVolModel class implements the EWMA volatility model in C++. Some specifications of the model include: a) I used the average of the first 500 squared log returns as the initial variance; 2) I used an lamda of .94 like RiskMetrics had suggested. 

3) RunningVol is the main file that runs the file reader on the CSV (openAndCloseData) that has the NASDAQ opening and closing prices and feeds the resutling vectors into the ewmaVolModel. 

** OUTPUT ** 

Hello!
This little project aims to show the evolution of varience using the EWMA Volatility Model.
The project's data comes from historical Nasdaq prices starting at 2020-11-13 and ending at 2025-11-12.
The initial varience is set as the average of the first 500 log returns squared.

Starting EWMA Volatility for NASDAQ Close Prices . . . . .

Today 500 day EWMA is: 0.000199595
Today 600 day EWMA is: 9.13322e-05
Today 700 day EWMA is: 0.000241247
Today 800 day EWMA is: 0.000396115
Today 900 day EWMA is: 0.000559404
Today 1000 day EWMA is: 0.00021006
Today 1100 day EWMA is: 4.6151e-05
Today 1200 day EWMA is: 0.000185557

 . . . . . Ending Close Prices EWMA

Starting EWMA Volatility for NASDAQ Open Prices . . . . .

Today 500 day EWMA is: 0.000205532
Today 600 day EWMA is: 6.87086e-05
Today 700 day EWMA is: 0.000223952
Today 800 day EWMA is: 0.000337365
Today 900 day EWMA is: 0.000461512
Today 1000 day EWMA is: 0.000240286
Today 1100 day EWMA is: 8.03276e-05
Today 1200 day EWMA is: 0.000167741

 . . . . Ending Open Prices EWMA

 ==========================================

Ending EWMA using closing prices is: 7.12604e-05

Ending EWMA using opening prices is: 7.7244e-05
