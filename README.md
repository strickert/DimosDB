# DimosDB

**Source Code is under embargo until October 2021**

DimosDB is a web application for managing, sharing, and querying differential mobility spectrometry data and metadata. The application is designed to reduce the time required to develop Differential Mobility Mass-Spectrometry (DMS-MS) and  Liquid-Chromatgrapy Differential Mobility Mass-Spectrometry (LC-DMS-MS) methods and simultaneously demonstrate the advantages of using non-traditional databases and modern web frameworks and libraries to create flexible and scalable web solutions to manage the rapidly increasing volume and complexity of MS data. The DimosDB platform is divided into three sections, presented in detail below, i.e., manage, compare, and optimize.


## Data management

Registered users can add, query, update, and delete DMS data and metadata from the underlying database directly through the web application. Every entry, or experiment, contains the CoV and FWHM obtained from the DMS peak of a particular compound analyzed with a specific modifier, instrument, and parameters set. Experiments are collected in the table illustrated below. Each column holds specific information about the experiment (i.e., analyte, modifier, instrument, and parameters preset), except for the rightest one, which includes options to delete, update and view the selected entry. Each entry is structured as follows: the top part of the page displays the DMS peak, as well as its CoV, FWHM, and resolving power (RP), while the bottom part contains additional information about the analyte, modifier, instrument.

![alt text](https://github.com/strickert/DimosDB/blob/main/figure_05.png)

## Compare and Optimize tools

In addition to DimosDB data management functionalities, the platform features two tools to manually compare DMS experiments and automatically find the best-suited modifiers for separating a predefined set of analytes. The former tool allows comparing the DMS peak of one or several compounds analyzed with the same or different analytical systems and cell parameters. This comparison tool can be used to find the most appropriate instrument or DMS parameters to analyze a defined set of compounds or explore the effects of different cell design and parameters values on the CoV. The optimization tool rank modifiers based on their ability to separate analytes using peak capacity (PC). For a defined set of compounds, PC is calculated as the absolute difference between the highest and lowest CoV values divided by the average FWHM.

<img src="https://render.githubusercontent.com/render/math?math=\Large PC = \frac{\left | CoV_{max} - CoV_{max} \right |}{\frac{1}{n}\sum_{i-1}^{n}FWHM_{i}}">


These tools are only accessible through the web application, and their interface is shown below. The optimization tool is illustrated below with five isobaric compounds: diphenhydramine, imidacloprid, ketorolac, lamotrigine, and phenyltoloxamine.

![alt text](https://github.com/strickert/DimosDB/blob/main/figure_06.png)

With a peak capacity of respectively 2.03 and 1.87, pure nitrogen gas and the 1.5\% chlorohexane modifier showed poor separation of these five isobaric compounds. In contrast, 1.5\% and 0.1\% isopropanol showed a much higher PC at respectively 6.95 and 11.81. Although 0.1\% of isopropanol gave the best separation for this particular set of compounds, other high-ranking modifiers should still be viewed as possible alternatives if the analyte signals show strong suppression by the volatile organic compound during DMS separation.

![alt text](https://github.com/strickert/DimosDB/blob/main/figure_07.png)
