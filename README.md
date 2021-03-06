# Election Analysis by Alec Ngai
## Project Overview
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes
2. Get a complete list of candidates who recieved votes. 
3. Calculate the total number of votes each candidate recieved. 
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; To achieve this, we will write a python script that will read a CSV file, and we will analyze the data and output the results to a TXT and terminal for the user to use. 

## Resources
- Data source: election_results.csv
- Software: Python 3.9.4, Visual Studio Code, 1.58.1

## Summary
The analysis of the election show that: 
- There were **"369,711"** votes cast in the election. 
- The counties were:
    - **Jefferson**
    - **Denver**
    - **Arapahoe**
- The counties results were:
    - **Jefferson** recieved **"10.5%"** of the vote and **"38,855"** number of votes
    - **Denver** recieved **"82.8%"** of the vote and **"306,055"** number of votes
    - **Arapahoe** recieved **"6.7%"** of the vote and **"24,801"** number of votes
- The largest county turnout was:
    - **Denver** recieved **"82.8%"** of the vote and **"306,055"** number of votes
- The candidates were:
    - **Charles Casper Stockham**
    - **Diana DeGette**
    - **Raymon Anthony Doane**
- The candidate results were:
    - **Charles Casper Stockham** recieved **"23.0%"** of the vote and **"85,213"** number of votes
    - **Diana DeGette recieved** recieved **"73.8%"** of the vote and **"272,892"** number of votes
    - **Raymon Anthony Doane** recieved **"3.1%"** of the vote and **"11,606"** number of votes
- The winner of the election was:
    - **Diana DeGette**, who received **"73.8%"** of the vote and **"272,892"** number of votes.

## Challenge Overview
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; In this challenge, we were given a pre-made Python file, where we had to add onto it, functionality of finding the counties and their specific vote counts to determin which county had the biggest turnout. 

![Intalize](https://github.com/alecngai/03-Election_Analysis/blob/main/Resources/Code_Initialize.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; To do this we intialized one list **county_options** and a dict **county_votes**, these will be used to store the data we gather from the main CSV.

![Intalize2](https://github.com/alecngai/03-Election_Analysis/blob/main/Resources/Code_Initialize2.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; To do this we intialized one list **winning_county** and a dict **winning_county_count**, these will be used to store the data we gather from the main CSV.

![GrabbingCounty](https://github.com/alecngai/03-Election_Analysis/blob/main/Resources/Code_GrabbingCounty.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; We just do a simple assignment of the row[1] into county_name variable, which will later be appended. The **for** loop will loop through the entire CSV which the county per row is stored in row[1]. We assign it to a variable just for it to be easier to read for the user. 

![GrabbingVotes](https://github.com/alecngai/03-Election_Analysis/blob/main/Resources/Code_GrabbingVotes.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Here we do an if statement to check if the county name exists within our list or not, if it is not in the list of counties, we add it to our list, then we also intialize the tracking for the vote. Afterwards we add a vote for that county. 

![AnalysisOutput](https://github.com/alecngai/03-Election_Analysis/blob/main/Resources/Code_AnalysisOutput.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; We then do the analysis of the votes to determin which county has the best turnout, we then have our winning_county, and winning_county_count, which are temporary storage variables we will overwrite with the highest count county. We then output to terminal, and also write to the TXT.

## Challenge Summary

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This script is very verstile as long as certain conditions are met. 

![FileToLoad](https://github.com/alecngai/03-Election_Analysis/blob/main/Resources/Code_FileToLoad.png)

1) The data must be in a CSV file format and have the same data format i.e. (Ballot ID,  County, Candidate), and the path to the CSV File must be the same as the path for the variable file_to_load, the output does not matter in this sense. 

![GrabbingData](https://github.com/alecngai/03-Election_Analysis/blob/main/Resources/Code_GrabbingData.png)

2) If the data format is different, we must edit two statements, and find the correct index value for where the data is stored.         

3) We must assume the data is clean, due to the way we wrote our code the data does not need to be sorted, however certain variables must be consistant, County & Candidate names must be the exact same case and same spelling, otherwise there will be duplicates due to the fact the code does not account for variations of spelling or capitilzation. 