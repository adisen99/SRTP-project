---
title : A session on Seismic data extraction and set-up 
numbersections: true
autoEqnLabels: true
date : 12/07/2020 
geometry: "left=3cm,right=3cm,top=3cm,bottom=3cm"
output: 
	pdf_document:
		template: NULL
---

# Understanding Earthquake Catalogue

- We study frequency magnitude relation given by the b-value of the seismic data equation. This lets us know the dangerous/hazardous regions.

- Many institutions/organisations have their seismic data properly catalogued which is also called the earthquake data catalogue available for download.

- We will use only one catalogue for the purpuses of our project namely that of the **International Seismological Center or ISC**

# Different Magnitude Scales

- Linear Magnitude Scale also called the Richter scale

$$M_l = \log{A} + 2.56\log{D} - 1.67$$

manly used for shallow events i.e. events with depth or epicenter distance less than 600 km. Also for magnitude higher than 8, the scale saturates and is not quite useful or representative of the data.

- Body wave Magnitude scale

$$M_b = \log{\frac{A}{T}} + \sigma \left( D, b \right)$$

It is maily used for Epi. Dist. less than 600 km. **Note that we will be using mainly this scale.**

- Surface Wave Magnitude scale

$$M_s = \log{\frac{A}{T}} + 1.66\log{\Delta} + 3.3$$

Which is also mainly used for Shallow events

- Moment-Madnitude scale (most commonly used)

$$M_w \approx \frac{2}{3}\log{M_0} - 6.06$$

In this magnitude relation, the physical parameters/factors such as rupture area and slip length are taken into consideration for calculating the earthquake magnitude.

**More information is present in the final Task-1 report**

# Process to Download Catalogue Data

- Go to the site `ds.iris.edu/gmap`. This gives a network of seismic stations. **This is only optional**

- Also we have the `isc.ac.uk/registration` for the same information about the seismic stations but for those used by the ISC for data cataloguing. 

- Now to download the data catalogue from ISC, go to the link `isc.ac.uk/iscbulletin/search/catalogue` and,

	- Group 9 (Andaman) -> Top Lat. = 13.734, Bottom Lat. = 10.275, Left Long. = 91.901, Right Long = 93.593

	- Group 2 (Western Himalayas) -> Top Lat. = 37.005, Bottom Lat. = 31.487, Left Long. = 73.268, Right Long = 79.706


- Enter the respective co-ordinates as mentioned in the previous point.

- Mention the start date as 1st Jan. of 1964, when the cataloguing had started till the present date.

- Take min. depth as 0 and max. depth as 6731 km which is the Radius of the Earth

- Min Magnitude = 0.1 and Max. magnitude as 10

- Choose Magnitude type as Body wave magnitude i.e. $M_b$ and select author as Any.

- Click output Event Catalogue and then copy the data and paste in Excel.

- Choose the Text to Column option in Excel and delimit the data using Tab and comma. After this clear everything after the Magnitude column. This step is called Data Cleaning.

- Plot the frequency vs. Magnitude curve after calculating frequency in Excel just to get a feel for the data.

- The actual plotting process will be carried using Zmap in MATLAB. One can use a Data analysis oriented programming language of their choice to visualise the data using Python or R.

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
