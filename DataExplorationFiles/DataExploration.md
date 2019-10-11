## DATA EXPLORATION – LINDA LORING FOUNDATION
For the study of different species and effects of temperature on them, we have been provided with different data sets including temperature and intensity at different date for various years with multiple sites. Here I have used R studios to pull some visualization graphs to understand some of the effects. I did use reading of one site for the year 2014.
### Making R read the csv file.
>TempData <- read.csv("C:\\Users\\tanis\\Desktop\\test.csv")

 ### 1) Scatterplot of temperature against date
![](https://github.com/rtanishkreddy/DataToDecision/blob/master/DataExplorationFiles/scatter_date_temp.png)
>ggplot(TempData, aes(y = Temp, x = Date)) + geom_points

It is easy to comprehend from the scatter plot so produced that the range of temperature was high with the start of the month (august) and it started to go down with time as date tends to reach later end of the month (September).
### 2) Scatterplot of Intensity against Temperature
![](https://github.com/rtanishkreddy/DataToDecision/blob/master/DataExplorationFiles/scatter_int_temp.png)
>ggplot(TempData, aes(y = Date, x = Intensity)) + geom_points

The above scatterplot represents how temperature variable depends on the intensity variable. With the increase in the temperature, the intensity started to vary and started to increase at the same time. With temperature being at the lower side, Intensity hence remained at the bottom of the graph showing that with the increase in the temperature, intensity tends to increase.
### 3) scatterplot with three variables 
![](https://github.com/rtanishkreddy/DataToDecision/blob/master/DataExplorationFiles/color_scatter_threevar.png)
>ggplot(TempData, aes(y = Temp, x = Date, color=Intensity)) + geom_point()

Considering all the three variables i.e., Temperature, Intensity, Date, and the color code that is given to the intensity variable, it is easy to comprehend how intensity depends on the temperature where upper end of the graph represents higher temperature and light blue dots represents higher degree of intensity. With more number of light blue dots being present at the upper area of the plot, we can say that higher temperature tends to higher degree of intensity.
### 4) temperature and intensity relation using the trend line

![](https://github.com/rtanishkreddy/DataToDecision/blob/master/DataExplorationFiles/temp_intesity_trend.png)
>ggplot(TempData,mapping=aes(Temp,Intensity),na.rm=TRUE) + geom_point()+geom_smooth()

To prove above inferences, I tried adding a trend line to the graph. Here with the increase in the temperature, the trend line which is representing the intensity variable goes upwards making it clear that intensity is directly dependent on temperature.
### 5)  Box plot with temperature and date

![](https://github.com/rtanishkreddy/DataToDecision/blob/master/DataExplorationFiles/boxplot.png)
>boxplot(TempData$Temp, ylab="Temperature", horizontal = TRUE)
Here, bar plot gives us a good idea considering it gives us an extra factor with the average. With this box plot, it shows that the mean temperature lies around 15 degree Celsius and most of the temperature set lying between 12 to 22.
