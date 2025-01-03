# AVDM Project: Competències Bàsiques

This project consists on analyzing the "Competències Bàsiques" data set in depth, with the aim of understanding the educational features of todays catalan pupils by studying the results of the different years final primary school and secondary school exams, also known as "Competències Bàsiques". Thus, we divide the work into four different parts that analyze in detail four specific features of the selected data set: the evolution of grades over time, the relationship between each student's grades for different subjects, the relationship between grades and financial investment, and the effects of promoting cultural events on students' scores.

The project relies on these open dataset repositories:
* Primary school: https://analisi.transparenciacatalunya.cat/d/rk5x-gny6
* Secondary school: [https://analisi.transparenciacatalunya.cat/d/59vm-wwq7\\]
* Investment: [https://analisi.transparenciacatalunya.cat/d/8spq-9nx7\\]
* Cultural events: https://analisi.transparenciacatalunya.cat/Cultura-oci/Agenda-cultural-de-Catalunya-per-localitzacions-/rhpv-yr4f
* Geography: https://www.icgc.cat/ca/Geoinformacio-i-mapes/Dades-i-productes/Geoinformacio-cartografica/Divisions-administratives

## Time evolution
The code regarding this topic can be found inside the folder Time evolution in the file "Time_evolution.ipynb" together with a folder with useful tools for the panda library from https://github.com/jvicens/analysis-and-visualization-of-big-data-course.git and a plot using Plotly library.

Structure of the code in "Time_evolution.ipynb":

-The average grades of every year students have been analyzed for the final secondary and primary school exams, obtaining the time evolution for every subject in both exams. This results in two plots: "sise.png" (primary school final exams) and "quart.png" (high school final exams) where the years are grouped in four years blocks for minimizing the effects of an extreme fluctuation from the general trend.

-For the mathematics subject, where the decrease between secondary and primary school is huge, the complete time line has been plotted for both primary and high school final exams, getting the plot "matemmatiques.png". This same procedure has also been done for the english subject, getting the "angles.png".

-Finally the average differences between secondary school final exams and primary school final exams have been plotted in "diferencia.png" for every four years block by representing the relative difference between the two exams with respect to the final secondary school grades.




## Subject Correlation
The code in the notebook 'subject_correlation.ipynb' is focused in trying to analize if there is a unique intelligence or if students present special talents and if talent in a subject can be related with talent in another. The notebook is divided in the following structure:

-Data Obtetention: Using an API, specified in the code.

-Data handeling: Selection of the columns needed, dropping NaN values, merging rows that come from the same student and creating new columns needed for the analysis. Selection of three samples from the datasets that will represent bad, average and good students.

-Correlation Matrix: Code to create plots that using heatmaps show the correlation for all dataset in the marks of different subjects. 

-Boxplots: Code to create the same boxplots that appear in the paper with all the necessary steps. They show the disperssion in the marks of different subjects for the three samples specified before.

-Radar plots: Code to create the same radar plots that appear in the paper. They show students who have specialized profiles or outsinding talents in one subject. I have added an extra radar plot for the sample of good students.

## Investment-Grades correlation
The question this part tries to solve is whether we can find any correlation between the educational attainment of private schools and the investment per pupil.

In the ``Ed_approach.ipynb'', we first show that studying private schools is representative of a significant proportion of catalan pupils. Then we show that there is no correlation between investment per pupil and educational attainment in the private schools.

Other jupyter notebooks are used to get introduced to plots and maps.

## Relationship between performance and cultural events

In "Cultura.ipynb" we try to obtain a relationship between the number of cultural events in Catalonia during the period of 2018-2023 and the results in "Competències Bàsiques". 

To do so, we firstly represent, by type, the number of events held each year. Due to a lack of information between 2018-2020, we center our analysis in the gap 2021-2023. In search of a linear behaviour, we represented  mean grades for both 6th Primary School and 4t Seconday School tests results of some subjects with the number of cultural events of certain type. The criteria for the pairing was the apparent relation between the former and the latter; for instance, we matched "Book" type events with the results in Catalan and Spanish. 
In this line, we also made graphics with the proportion of students with good grades (above 75) in a subject and the proportion of cultural events of a particular type by region. 

Because in the analyses we did not obtain a conclusive linear fit nor a similar behaviour in the decayment, respectively,  we  concluded that cultural events and performance in Competències bàsiques are not correlated. 

## Acknowledgements 

This codes and materials have been created and developed by the collaborators Eduardo Dejuán Bitria (edejuan2002), Andreu Rocamora Martorell (AndreuRocamora), Andrea Cera Palatsi (acerapal) and Judith López Zancajo (Jud0-0). 
