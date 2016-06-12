The present file describes the different scripts asked for the creation of four different graphs of this project. 

Each graph is defined in a separate file plot1.R, plot2.R, plot3.R, plot4.R. The output of each graph will be put in a separate file under png file.
This assumes that the data file has been extracted and copied to the current folder.

Each .R file can be run independently from the others. Howevern I have loaded the entire data set and filtered it after, as I did not manage to do it 
at the same time

Each .R file is divided in 2 parts :

## Step 1 : Acquire, format, and filter the data

The data are loaded under character format, and not as factors. The conversion under character format is easier to convert the data under numeric or Date/Time types. 
For example, the conversion from factor to numeric class give the reference of the corresponding class, and not the real value.
	
The data are then converted to the appropriate data types (numeric or date/time).  The first two column are merged to a single date_time field to  benefit from the properties of lubridate library. 
During the conversion, R generates NA values for each original '?' value in the source file. The corresponding lines are then removed from the Data frame, as they are not complete.

All the column are then merged to a single data frame. 

At last, this data frame is filtered to keep the rows corresponding to the requuired dates (Feb 1sr, 2007 and Feb 2nd, 2007).
	
## Step 2 : Draw the graphs

This step is dedicated to the construction of the graphs (one per .R file). Each file will be saved under a .png file, with same base name as the .R file.