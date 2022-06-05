# Bikesharing

## Overview
In this project Tableau is the main pprogram that is used to create visualization using data from citibike data in NYC. We downloaded the *201908-citibike-tripdata*, which would be used to create visuals using Tableau. Before using the *201908-citibike-tripdata* first we needed to convert the tripduration to datetime using Jupyter Notebooks and pandas, after converting the tripduration column to datetime, we exported the updated table(*201908-citibike-tripdata_UPDATE*) to our working folder and use the updated csv to Tableau. In Tableau we would create 5 different worksheets which would contain our visualizations, which are 2 line graphs, and 3 heatmaps. After those were created we then added panels to orginize the worksheets that we created into 2 seperate panels, one for the line graph and the other panel for the heatmaps. And we then saved the project to Tableu Public, link will be added at the bottom.
## Results
### Code Conversion:
First we used JupyterNotebook to get the *201908-citibike-tripdata* and read the data into a dataframe.
![JN1](https://user-images.githubusercontent.com/97326526/172066630-701bc583-fe0d-4413-ba28-46accec499a1.JPG)
After adding the original csv file into the program we would need to convert a specific column from the trip data, the need column would be the tripduration. We convert the tripduration to a datetime datatype, then checking the datatypes of the column by using **.info()** function. After confirming the datatype has been changed then, exporting the new dataframe into a updated csv file without the index.
![JN2](https://user-images.githubusercontent.com/97326526/172066775-583c4aab-2ee2-46a9-a8e7-88538dcaed27.JPG)
### Tableau Visualizations
> - **Worksheet One:**
The very first visualization completed was the Chechkout Times for Users, for this we would use the updated tripduration column in the columns row, we would have 2 columns of tripduration one using hours, and the other using minutes for it measurement the minute tripduration column would also be set to continuous. The Rows will use the count of bikes that in our data, so either bike_id or using )the tripdata was used in the rows column. The Hour tripduration was also used as the filter for the line graph.
![Checkout_Users](https://user-images.githubusercontent.com/97326526/172067174-8ada5abc-cfdc-4d8e-b977-198091cbde79.JPG)
> - **Worksheet Two:**
> The second visualization will use the very same premise of the first line graph exepct there is more data added into in this worksheet is called Checkout Time by Gender. In this worksheet we created a calculated field that would turn the genders column numbers which reperesent Uknown, Male, and Female with number which are 0, 1, 2. The calculated field is as follows **If [Gender]='0' then 'UNKNOWN' ELSEIF [Gender]='1' then 'MALE' ELSEIF [Gender]='2' then 'FEMALE' END** the calculated field is called Number to String since it converts the numbers to a string value. The numbers to string column is the added as a color in the marks section and also added into filters.
![Checkout_Gender](https://user-images.githubusercontent.com/97326526/172067390-68e21a7f-6a00-4350-950d-1c6748491b57.JPG)
> - **Worksheet Three:**
The third worksheet contains a heatmap and its called Trip by Weekend for Each Hour, in the column section of the heatmap it useds the Stoptime column and is set to Weekday, and the row uses the Startime column and is set to use hours, with the count being from the tripdata we use this in the color in the marks. The default color was blue so it was changed to a orange to red color scheme.
![Trip_by_Weekend](https://user-images.githubusercontent.com/97326526/172067762-5a55e855-2eef-4537-bb93-00d82ab4747c.JPG)
> - **Worksheet Four:**
The second heatmap shows the Trip by Gender(Weekday per Hour) which is also the name of the worksheet for the heatmap. The heatmap columns has the Number of String column which is the Gender conversion column,and the Stoptime column which used the weekday as its time. And the rows for the heatmap is the Starttime and used the hour as it time, and just as for the first heatmap the the count from the tripdata is used for the color in the marks section.
![Trip_by_Gender](https://user-images.githubusercontent.com/97326526/172068120-f2b5a507-6cf1-442c-b980-9f3985639760.JPG)
> - **Worksheet Five:**
The final
