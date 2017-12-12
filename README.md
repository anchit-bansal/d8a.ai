# d8a.ai
This repository is an internship assignment submission to d8a.

Contents are:

  airports.csv #Departure from Delhi and list of arrival airports
  airports_arrive.csv #Arrival at delhi
  airports1.csv #Original airports file
  code.ipynd #Code

Code file is a Ipython notebook.

  1st cell is the header part importing all requiered libraries.
  
  3rd cell is the cleaning code:
     Here the original airports file was cleaned based on Nan values in "iata_code" and "type" columns. Further on the airports of  "type" heliport, small_airport, medium_airport outside of India are also scrapped out for ease in computation, the only medium and small airports allowed are the Indian Airports.(Also the only "Non_stop" flights are included as the they will overlap with the flights with the stops and become redundant).
  
  2nd cell the is the actual computation part:
    parse(source,destination,date) function:
      Here a general link to Expedia website is put in ulr variable with source and destination ports being changed in every computation. Code gets response from the link and gets all flight information in Json format and returns it.
    main part:
      The extracted data is filtered according to the departure and arrival time of flights at Derlhi airport and summed up.
    The result is the total number of flights on 20/12/2017 arriving on or departing from Delhi airport.
