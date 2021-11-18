# Student-Enrollment-Project
## Background
After the first death in California of an elderly male, Governor Newsom declared a state of emergency to halt in-person instruction in an effort to stop the spread of Covid-19. Shutdown had a major impact on families. On February 2020: Cases have fallen dramatically prompting schools to reopen. On Oct 2021: Mandate to have children vaccinated by Jan 2022. 

## Research Questions
  * How many students were enrolled per county?
  * What was the significant change of enrollment pre-Covid vs during Covid?
  * Did enrollment numbers change due to demographics?
  * Is there a correlation between COVID cases vs students enrolled?

## Student Enrollment situation pre-Covid vs. post-Covid
### Students with Disabilities
|CountyName  |EnrollTotal_2020| 	Students with Disabilities_2020 |	EnrollTotal_2021 |	Students with Disabilities_2021 |	percent_2020 	|percent_2021	|		
| :--------: | :------------: | :-------------------------------: | :--------------: | :------------------------------: |:-----------: |:-----------: |
|**Alameda** |222812 	        |24319 	                            |218094 	         |24977 	                          |%10.91 	      |%11.45       |
|**Alpine**  |70 	            |12 	                              |73 	             |11 	                              |%17.14 	      |%15.07       |
|**Amador**  |3958 	          |523                                |3889 	           |750 	                            |%13.21 	      |%19.29       |
|**Butte** 	 |28777 	        |3558 	                            |27794 	           |3651                     	        |%12.36 	      |%13.14       |
|**Calaveras** 	 |4885 	          |805 	                          |4543 	           |760 	                            |%16.48 	      |%16.7        |

The above summary table has encoded the percentage of Students with Disabilities, and there isn't a significant percentage difference from pre-Covid to post-Covid


|Total Enrollment in 2020 |Total Enrollment of Students with Disabilities in 2020 |Percent of Students with Disabilities in 2020|Total Enrollment in 2021|Total Enrollment of Students with Disabilities in 2021|Percent of Students with Disabilities in 2021 |Average percentage differnce|
| :--------: | :------------: | :------: | :------: | :-----: |:------: |:---: |
|6038302 	   |695002 	        |%11.51 	 |5873395 	|721204 	|%12.28 	|%0.83 |

The calculated average percentage difference shows a slight increase in the number of total enrollments of _Students with Disabilities_ post-Covid.

```python
  avgDiff = (disable_df["percent_2021"] - disable_df["percent_2020"]).sum()/len(disable_df)
```

#### Bar charts of total enrollments vs total enrollments of Students with Disabilities 
![image](https://github.com/ludanzhan/Student-Enrollment-Project/blob/main/Images/Disable.png)
#### Bar charts of total enrollments vs total enrollments of Students with Disabilities in each county
![image](https://github.com/ludanzhan/Student-Enrollment-Project/blob/main/Images/DisableSUM.png)

Both graph doesn't show a siginicatn change in total enrollments of _Students with Disabilities_

### Socioeconomically Disadvantaged Students
|CountyName  |EnrollTotal_2020| 	Students with Disabilities_2020 |	EnrollTotal_2021 |	Students with Disabilities_2021 |	percent_2020 	|percent_2021	|		
| :--------: | :------------: | :-------------------------------: | :--------------: | :------------------------------: |:-----------: |:-----------: |
|**Alameda** |222812 	        |24319 	                            |218094 	         |24977 	                          |%42.74	        |%41.58       |
|**Alpine**  |70 	            |43 	                              |73 	             |45 	                              |%61.43  	      |	%61.64      |
|**Amador**  |3958 	          |1607                               |3889 	           |1674 	                            |%40.60 	      |%43.04       |
|**Butte** 	 |28777 	        |17222	                            |27794 	           |16940                   	        |%59.85 	      |%60.95       |
|**Calaveras** 	 |4885 	      |2511	                              |4543 	           |2251	                            |%51.40 	      |%49.55       |

The above summary table has encoded the percentage of Socioeconomically Disadvantaged Students, and there isn't a significant percentage difference from pre-Covid to post-Covid

|Total Enrollment in 2020 |Total Enrollment of Socioeconomically Disadvantaged students 2020|Percent of Socioeconomically Disadvantaged students in 2020 |Total Enrollment in 2021 |Total Enrollment of Socioeconomically Disadvantaged students in 2021 |Percent of Socioeconomically Disadvantaged students in 2021 |Average percentage differnce|
| :--------: | :------------: | :------: | :------: | :-----: |:------: |:---: |
|6038302 	|3663287 	|%60.67 	|5873395 	|3542861 	|%60.32 |	%-0.41|

The calculated average percentage difference shows a slight decrease in the number of total enrollments of _Socioeconomically Disadvantaged Students_ post-Covid.
```python
  avgDiff_socio = (social_df["percent_2021"] - social_df["percent_2020"]).sum()/len(social_df)
```

#### Bar charts of total enrollments vs total enrollments of Socioeconomically Disadvantaged Students
![image](https://github.com/ludanzhan/Student-Enrollment-Project/blob/main/Images/Socio.png)
#### Bar charts of total enrollments vs total enrollments of Socioeconomically Disadvantaged Students in each county
![image](https://github.com/ludanzhan/Student-Enrollment-Project/blob/main/Images/SocioSUM.png)

Both graph doesn't show a siginicatn change in total enrollments of _Socioeconomically Disadvantaged Students_

### Migrant Students
The data held demographics and a comparison between 2020 and 2021, specifically focused on _migrant students_.

|CountyName  |EnrollTotal_2020 	|Migrant_2020 	|EnrollTotal_2021 	|Migrant_2021 	|Percent Total 2020 	|Percent Total 2021
| :--------: | :------------: | :------: | :------: | :-----: |:------: |:---: | 						
|Alameda 	   |222812 	        |989 	     |218094    |855 	    |44.39%   |	39.2033%|
|Alpine 	   |70 	            |0 	       |73 	      |0 	      |0.000000 |	0.000000|
|Amador 	   |3958 	          |0 	       |3889      |0 	      |0.000000 |	0.000000|
|Butte 	     |28777 	        |123 	     |27794 	  |67 	    |42.74%   |	24.105%|
|Calaveras 	 |4885 	          |0 	       |4543 	    |0 	      |0.000000 |0.000000|

Preview of the summary table shows a slightly decrease in total number of enrollments of _migrant students_.

|Total Enrollment 2020 	|Total Migrant 2020 	|Percent of Migrant 2020 	|Total Enrollment 2021 	|Total Migrant 2021 	|Percent of Migrant 2021|
| :--------: | :------------: | :------: | :------: | :-----: |:------: |
|6,038,302.00 	        |47,268.00            |0.783% 	                |5,873,395.00 	        |46,409.00 	          |0.790%|

The total number of enrollments of _migrant students_ doesn't change significantly.


#### Bar charts of total enrollments vs total enrollments of migrant students
![image](https://github.com/ludanzhan/Student-Enrollment-Project/blob/main/Images/Migrant.png)

#### Bar charts of total enrollments vs total enrollments of migrant students in each county
![image](https://github.com/ludanzhan/Student-Enrollment-Project/blob/main/Images/MigrantSUM.png)


Both graph doesn't show a siginicatn change in total enrollments of _Migrant Students_

### Students in Foster Care
The data held demographics and a comparison between 2020 and 2021, specifically focused on _Students in Foster Care_.


|CountyName 	|EnrollTotal_2020 	|Foster Care_2020 	|EnrollTotal_2021 	|Foster Care_2021 	|Percent Total 2020 |	Percent Total 2021	|		
| :---------: | :---------------: | :---------------: | :---------------: | :---------------: |:-------------: |:-------------: |
|Alameda 	    |222812 	          |402 	              |218094 	          |442                |0.18% 	         |0.2026%|
|Alpine 	    |70 	              |2 	                |73 	              |0 	                |2.857%          |0.000000|
|Amador 	    |3958 	            |19 	              |3889 	            |23 	              |0.48%	         |0.591%|
|Butte 	      |28777 	            |247 	              |27794 	            |245 	              |0.858%	         |0.8814%|
|Calaveras 	  |4885 	            |70 	              |4543 	            |40 	              |1.432%	         |0.88%|


Preview of the summary table doesn't show significant change in total number of enrollments of _Students in Foster Care_.


#### Bar charts of total enrollments vs total enrollments of Students in Foster Care
![image](https://github.com/ludanzhan/Student-Enrollment-Project/blob/main/Images/Foster.png)

#### Bar charts of total enrollments vs total enrollments of Students in Foster Care in each county
![image](https://github.com/ludanzhan/Student-Enrollment-Project/blob/main/Images/FosterSUM.png)

Both graph doesn't show a siginicatn change in total enrollments of _Students in Foster Care_

### Students Race/Ethnicity

|Race 	           |Percent 2020 	|Percent 2021 	|Total Count 2020 	|Total Count 2021 	|Percentage Point Diff|
| :--------------: | :----------: | :-----------: | :---------------: | :---------------: |:------------------: |
|African American  |5.22% 	      |5.11% 	        |315128 	          |300244 	          |-0.106885%|
|American Indian 	 |0.49% 	      |0.47% 	        |29464 	            |27558 	            |-0.018751%|
|Asian 	           |9.43%        	|9.62% 	        |569119 	          |565295             |0.199522%|
|Filipino 	       |2.40% 	      |2.40% 	        |144864 	          |140952 	          |0.000754%|
|Hispanic 	       |54.88% 	      |55.35% 	      |3313650           	|3251013 	          |0.474331%|
|Pacific Islander  |0.44% 	      |0.46% 	        |26769 	            |25823 	            |0.012447%|
|White 	           |22.36% 	      |22.99% 	      |1350166         	  |1272890            |0.627801%|
|Two or More Races |3.94% 	      |4.09% 	        |237658 	          |240477      	      |0.158503%|
|Not Reported 	   |0.85% 	      |0.84% 	        |51484 	            |49143 	            |-0.015919%|

The summary table shows a slightly difference among each race


