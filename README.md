# Recruitment-data-analysis-task

#Task 1

Based on the pandas and faker libraries implement a function named generate_ssns , which returns an object of the Series type with the number of records specified by the function input parameter and values representing the random numbers generated PESEL.

Implement the generate_unique_ssns function (in any way), which returns an object of the Series type with the number of records specified by the input parameter of the function and values representing random and unique (only within the returned collection) PESEL numbers appropriate for people of gender (female / male) and born in the range of dates (from-to) also specified by the input parameters of this function.

Then implement the calls to the generate_ssns and generate_unique_ssns functions for 1,000, 10,000, and 100,000 records, indicating the selected gender and the range of birth dates from 1990-01-01 to 1990-01-19. Make a measurement and display the duration of their execution (separately for each call of each of these two functions).

Implement a function called validate_ssn , which takes the PESEL number as input along with the expected gender (female / male / any) and date of birth (specific / specific or any), and returns information on the correctness of the PESEL number on the output. Inside the function, include the logic verifying the syntactic correctness of the PESEL number, taking into account the information about the expected gender and date of birth. Then test the validate_ssn function with sample data.

#Task 2

1. Using sqlite3 , create a new database with the FlightLeg table , which will contain information about the flights of the planes, with the following columns:  
  * id - numeric identifier assigned from the sequence  
  * tailNumber - aircraft identifier  
  * sourceAirportCode, destinationAirportCode - three-letter airport code (according to IATA)  
  * sourceCountryCode, destinationCountryCode - three-letter country code (according to ISO 3166-1 Alpha-3)  
  * departureTimeUtc, landingTimeUtc - date and time (accurate to the second), respectively, of departure and landing (in UTC)  

2. Fill in the FlightLeg table with data from the file: https://bitpeak.pl/datasets/flightlegs.csv  

3. Add two new columns to the table:  

  * flightDuration - fill it with values ​​representing flight duration in minutes (rounded to the nearest integer)  

  * flightType - fill it with the flight type values: domestic (value 'D' = domestic) or foreign (value 'I' = international); a domestic flight is a flight that begins and ends in the same country  

4. Implement the logic that answers the following questions:  
  1. Which aircraft made the most flights?  
  2. Which plane flew the most minutes?  
  3. Which flight, broken down into domestic and foreign ones, was the shortest and which was the longest, and how many minutes was it?  
  4. (optional) How many erroneous flight records are there, which indicate that the aircraft was performing more than one flight at the same time? View all pairs of such conflicting flights.  
