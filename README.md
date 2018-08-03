# Sensitivity_Analysis_of_fWAR
  In order to test the sensitivity of the predictive ability of the equation for position player fWAR, I made several radical and theoretically impossible changes to values in said equation. Those changes include:
  - Setting the linear weights in wOBA to impossible run values. (i.e. a run value of 5 for a homerun or 2 for a walk)
  - Setting the Runs per Win value to 20, which is about twice the value fangraphs.com uses.
  - Giving fielding runs 5 times more weight by multiplying the value by 5 in the equation.
  
  I, then, performed a bootstrapped ridge-regression 10,000 times and stored the beta values. After graphing the beta values for the different fWARs, it is very clear that none of them are statistically significantly different in their ability to predict team wins. 
 
## Data
### The data used for this are taken from a variety of places that are listed below with the date acquired. The data sets themselves are not included to ensure compliance with the terms of use of the different destinations. 
- fangraphs.com 2017 "batting leaders" page for all players with team splits and a plate-appearance minimum of 0 in a custom table with the following stats: Name, Team, G, AB, PA, H, 1B, 2B, 3B, HR, R, RBI, BB, IBB, SO, HBP, SF, SH, GDP, SB, CS, OBP, wOBA, RE24, wSB, UBR, wGDP, wRAA, wRC, Bat, Fld, Rep, Pos, RAR, and WAR. (07/16/2018)
- the fangraphs.com fielding data set from the 2017 "batting leaders" page for all players with team splits and a plate-appearance minimum of 0. The table needed is the page default. (07/16/2018)
- a data set with only team wins taken from baseball-reference.com (06/19/2018)
