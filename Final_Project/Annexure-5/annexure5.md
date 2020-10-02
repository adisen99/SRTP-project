---
title : Annexure - 5 - Survey forms, questionnaires and/or consent form
numbersections: false
geometry: "left=3cm,right=3cm,top=3cm,bottom=3cm"
output: 
	pdf_document:
		template: NULL
---

# Process to Download Catalogue Data

- We downloaded the data from the ISC catalog`isc.ac.uk/registration` for the same information about the seismic stations but for those used by the ISC for data cataloguing. 

- Now to download the data catalogue from ISC, I went to the link `isc.ac.uk/iscbulletin/search/catalogue` and downloaded the data for the Andaman region with the follwing co-ordinates

	- Group 9 (Andaman) -> Top Lat. = 13.734, Bottom Lat. = 10.275, Left Long. = 91.901, Right Long = 93.593

- Entered the respective co-ordinates as mentioned in the previous point.

- Mentioned the start date as 1st Jan. of 1964, when the cataloguing had started till the present date.

- Took min. depth as 0 and max. depth as 6731 km which is the Radius of the Earth

- Min Magnitude = 0.1 and Max. magnitude as 10 were taken

- Chose Magnitude type as Body wave magnitude i.e. $M_b$ and selected author as "Any".

- Clicked output Event Catalogue and then copied the data and pasted in Excel.

- Chose the Text to Column option in Excel and delimited the data using Tab and comma. After this cleared everything after the Magnitude column. This step is called Data Cleaning.

- Ploted the frequency vs. Magnitude curve after calculating frequency in Excel just to get a feel for the data.

- The actual plotting and analysis process was carried using Zmap in MATLAB. One can use a Data analysis oriented programming language of their choice to visualise the data using Python or R. The data was further cleaned by me to make suitable for Zmap compatibility using the Pandas library of Python

# Error for small datasets.

$> 2000$ good quality earthquakes are required for 98% confidence in the final data results.

---------------------------
 N (frequency)    B value
--------------- ----------- 
      500        0.91-1.12

	  100        0.86-1.20

	   50		 0.50-1.49

	   30		 0.70-1.74

---------------------------

# Objective of data-

The data was collected to analyse the seismic data and obtain the Frequency-Magnitude Distribution curve which was then fitted to the theoretical Gutenberg-Richter relation to obtain the b-value and subsequantly the spatio-temporal variation of b-value. These plots were then analysed and suitable inferences were made in reference to hazard estimation of the Andaman Region
