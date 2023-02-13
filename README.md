# Counting-Crow-de-s
This program is used to parse through CSV's that have a ZipCode header and return the number of addresses each zipcode has. To use this program simply open the file with a browser. Open the developer tools (either right click and hit inspect) or press (F12). Upload a csv and click submit. Results are printed to the console.

It is important to note that this is a running total meaning that if you add two csv files, it will show you the total zipcodes for both files. Click clear before you submit another CSV if you are looking to have seperate results.

There is a line in the code that has been commented out that would allow you to look at how many instances of a specified zipcode are in a CSV. It was used for testing but may be useful. Additionally, this program does not have any conditional logic for addresses that have a zipcode but are null or blank.

I used PapaParse instead of FileReader to streamline the code. Inititially I had used a for loop to count the number of zipcodes, however there's more flexibility and clarity in the results using .reduce(). The .reduce() funtion tallied the number of occurances and returned an object that was stored in a map. {zipcode, (number of instances)}. The current format allows you to have all csv data in one result. As you add csv files the results will grow, or you can clear between uploads and have a new results map. The results map is called zipCodeData.


