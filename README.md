# Election Analysis

## Overview of Election-Audit

### Purpose
The purpose of this analysis is to assist Tom, a Board of Elections employee, with an election-audit of the tabulated results for US congressional voting district in Colorado. His manager, Seth, is asking to automate the process using Python and report the results to a text file. After all votes are counted, we need to generate a vote count report to certify this US congressional race.

## Election-Audit Results

### Sources and Files
* The election-audit analysis is based on the following data source: [election_results](Resources/election_results.csv).
* The completed election-audit analysis is available here: [PyPoll_Challenge](PyPoll_Challenge.py).
* The election-audit analysis script saved to a text file is available here: [election_results](Analysis/election_results.txt).

### Software
The software used to write, edit, save and execute scripts for this analysis were:
* Python 3.9.7
* Visual Studio Code 1.62.3

### Outcomes

Below address the following election outcomes. Use images or examples of your code as support where necessary.

* How many votes were cast in this congressional election?
The total votes in this congressional election were 369,711.  

* Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
The county votes are as follows:

[County_Votes](County_Votes.png)

To generate this county list with its respective number of votes and the percentage of total votes we had to create a county list and county votes dictionary in the Python script:
```
county_list = []
county_dictionary = {}
```

We had to use a **for loop** to get the county from the county dictionary.
```    
    for county_name in county_dictionary:

        countyvotes = county_dictionary.get(county_name)

        countyvote_percentage = float(countyvotes) / float(total_votes) * 100

        county_results = (
            f"{county_name}: {countyvote_percentage:.1f}% ({countyvotes:,})\n")
        
        print(county_results, end="") 
```

* Which county had the largest number of votes?
* Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
* Which candidate won the election, what was their vote count, and what was their percentage of the total votes?

## Election-Audit Summary
Election-Audit Summary: In a summary statement, provide a business proposal to the election commission on how this script can be used—with some modifications—for any election. Give at least two examples of how this script can be modified to be used for other elections.
