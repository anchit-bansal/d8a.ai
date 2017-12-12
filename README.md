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

# 2nd Assignment
Files for 2nd assignment:

omr.ipynb
omr_pic.jpg

omr_pic.jpg picture is the omr sheet input with darked circles.

# omr.ipynb:
cell 1:
Importing required libraries.

cell 2:
Reading image and converting in gray color format.

cell 3:
Detecting the page in the image.

cell 4:
Cropping out the detected paper in the image.

cell 5:
Display paper.

cell 7:
Doing binarification of the extracted paper.

cell 8:
Display binary image.

cell 9-12:
Getting height and width.

cell 13-14:
Cropping out 1st column of answers.

cell 15-16:
Cropping out 2nd column of answers.

cell 17-18:
Cropping out 3rd column of answers.

cell 19-20:
Cropping out 4th column of answers.

cell 21-25:
Extracting all the question rows from the extracted columns and aggregating them in a list.

cell 26:
From the list of extracted questions finding the filled circle.
All the circles are extracted present in the question row and a cirle mask is created. Iteration is performed over all the circles in the row and bitwise and is performed with the mask, number of nonzero pixels are extracted from the output of bitwise and and the contour with max number of non zero pixels is the darkened circle. That particular bubble is marked green. 
