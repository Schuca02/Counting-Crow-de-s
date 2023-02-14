# Counting-Zip-Crows
**Purpose**

This program is used to parse through CSVs that have a ZipCode header and return the number of addresses each zip code has in a map called zipCodeData. 

If a CSV line item does not have a zip code (i.e., it is null or blank), there is no additional logic to look up the address’s zip code. Instead, it is skipped.


**How to run this project**

To run this program, open the file in your browser. Open the developer tools (Right click the webpage and hit “inspect”) or press F12. Upload a csv and click submit. Results are printed to the console.

It is important to note that each additional CSV you add will contribute towards the same zip code tally. I.e., it will show you the total zip codes for both files. Clicking “clear” will flush the results and create a new output.


**Miscellaneous Notes**

I used the PapaParse library instead of the often-used FileReader to simplify the code. Initially, I used a for-loop to count the number of zip codes. The PapaParse .reduce() function tallies the number of occurrences and returns an object that is stored in a map {zip code, (number of instances)}. This allows you to have all csv data in one map. Using .reduce() ultimately reduces verbosity (pun intended). 
