# Data Entry Analysis

## Study

Records have been collected regarding of the micro organisms called "plaktron' which are found in water sources and are food to 
different larger aqutic organisms. Samples are collected at different times at different depths for many years. Ultimate study is to find 
a analysis individual count at give temp, time and depth.

## Problems assosisated with Given Data Sets

- Date format not defined well and is unclear. Format must be specified either as MM/DD/YY or DD/MM/YY or so.
- Several headers are not defined and difficult to interpret. 
- Unit of the headers "temp" and "density" not defined. It ca be read in Fahrenhite/Celcius or individual per unit volume respectively.
- many cells have Missing values.
- Few roW are not decribed. Ex- I4 in zoop-temp
- As given that study will focus on variation in density between day and night, table does not specify which was recorded at what time,
and therefore there must be an extra header specifiying time.
- There are couple of negative values for "chippo #/L", which makes no sense and may hinder the result.
- Two different tables for same reading headers not needed. Increases redundancy.

## Solving Issues for better study

- Add time column for better understanding.
- Specify the format for dates and time.
- Specify units for depth, temperature, Density etc.
- For every blank cell, using "average" function in excel to add that calculated value or replacing it with
"NA" will prevent tables hinder study.


## re-creating table format

| Date (MM/DD/YY) | Time (HH:MM) | Depth in meters | Temperatre in Celcius | Density per litre | Colony diamter in cm sq | Species |
|-----------------|--------------|-----------------|-----------------------|-------------------|-------------------------|---------|
| 6/5/2010        | 12:00        | 0.5             | 15.2                  | 76                | 3.22                    | cuni    |
| 6/5/2010        | 17:00        | 5               | 13.7                  | NA                | NA                      | cuni    |
| 6/18/2010       | 21:28        | 50              | 18.1(average)         | NA                | NA                      | chippo  |

| Date (MM/DD/YY) | Time (HH:MM) | Depth (meters) | Cuni individuals/L | Cuni Colony size (cm) | Chippo individuals/L | Chippo colony size (cm) | Chla | Temperature (Celcius) |
|-----------------|--------------|----------------|--------------------|-----------------------|----------------------|-------------------------|------|-----------------------|
| 06/04/2011      | 19:34        | 0.5            | 72                 | 2.12                  | 45                   | 2.56                    | 3.1  | 14.1                  |
| 08/08/2011      | 06:18        | NA             | 2.60 (average)     | NA                    | NA                   | 3.22                    | 3.22 | 25                    |

