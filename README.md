# Election Analysis

## Overview of Project

### Purpose
The purpose of this stock analysis report is to help Steve, a recent business school graduate, evaluate multiple stocks for his parents who are interested in investing in green energy. 

Overview of Election Audit: Explain the purpose of this election audit analysis.

## Results
The election analysis is based on the following file: [election_results](Resources/election_results.csv).

Election-Audit Results: Using a bulleted list, address the following election outcomes. Use images or examples of your code as support where necessary.

* How many votes were cast in this congressional election?
* Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
* Which county had the largest number of votes?
* Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
* Which candidate won the election, what was their vote count, and what was their percentage of the total votes?


* The following code is used to implement this feature in the VBA script:

```
yearValue = InputBox("What year would you like to run the analysis on?")
```


* To calculate the yearly return in the VBA script the following line of code was added:
 
```
Cells(4 + i, 3).Value = tickerEndingPrices(i) / tickerStartingPrices(i) – 1
```

* However, we first had to find the tickerStartingPrices as well as the tickerEndingPrices to get the yearly return. These lines of codes were used with an **If-Then statement** as shown below:

```
If Cells(i - 1, 1).Value <> tickers(TickerIndex) And Cells(i, 1).Value = tickers(TickerIndex) Then
     
     tickerStartingPrices(TickerIndex) = Cells(i, 6).Value

End If

If Cells(i + 1, 1).Value <> tickers(TickerIndex) And Cells(i, 1).Value = tickers(TickerIndex) Then
     
     tickerEndingPrices(TickerIndex) = Cells(i, 6).Value
                
TickerIndex = TickerIndex + 1
            
End If
```

* The block of code above is performed inside a for loop and the TickerIndex was set to equal to zero before it loops over the rows of stocks.


## Summary
Election-Audit Summary: In a summary statement, provide a business proposal to the election commission on how this script can be used—with some modifications—for any election. Give at least two examples of how this script can be modified to be used for other elections.
