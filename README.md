<h1 align="center">ETL and EDA Project: Vehicle Reviews</h1>
<p align="center">
  <img src="https://s19538.pcdn.co/wp-content/uploads/2018/01/Edmunds-Logo.jpg" alt="Vehicle Reviews" width=auto height="150" style="border-radius: 10px;">
</p>

<hr/>

<h3>Context and introduction to the project:</h3>

EThis project consists of a **ETL** (Extraction, Transformation, Loading) and **EDA** (Exploratory Data Analysis) process of a dataset that contains consumer's thought and the star rating of car manufacturer/model/type, from Edmunds (buying, selling and reviews of cars platform). This dataset contains reviews from January 30th, 2002, to September 19th, 2018.

<h3>Project steps:</h3>

**1°**  
The data from the Kaggle platform was downloaded, link to the page <a href="https://www.kaggle.com/datasets/ankkur13/edmundsconsumer-car-ratings-and-reviews">HERE</a>. The data came in a .zip file that was manually unzipped to the "Raw data" directory, within the "Dataset" folder. The .zip file was then deleted. The datasets were in CSV files according to vehicle brand. We begin by unifying all these datasets into a single file in PARQUET format called "car_reviews.parquet". This process was carried out on the notebook "[1-file_merge.ipynb](1-file_merge.ipynb)". Due to errors in the original data format, some registers (reviews) were lost. These losses are specified in said notebook.

**2°**  
Secondly, we performed a cleaning and transformation of the data: we divided the "Vehicle_Title" column into multiple columns that indicate characteristics of the vehicle (make, model, year, engine, body), from the "Review_Date" column only the date, since the schedule seemed not relevant information. This process was carried out on the notebook "[2-cleaning_and_EDA.ipynb](2-cleaning_and_EDA.ipynb)".  

**3°**  
Finally, we carry out the Exploratory Data Analysis, in which we investigate the variables, missing values, time information, and some metrics in relation to brands, models, and propulsion (electric/hybrids/gas vehicles). This process is also found in the notebook "[2-cleaning_and_EDA.ipynb](2-cleaning_and_EDA.ipynb)".

<h3>Used tools:</h3>  
Python with libraries like Pandas, re, os, csv, Matplotlib and Seaborn.

<h3>Data dictionary:</h3>

- Review_Date: date of the review in year/month/day format.

- Author: name of the author.

- Brand: brand of the car.

- Model_Name: car model.

- Model_Year: production year of the car.

- Mecanic_Details: displacement, number of cylinders, transmission.

- Body_Type: body type of the car and number of doors.

- Full_Description: all the previous information about the car together.

- Rating	qualification: from the reviewer between 1 (bad) and 5 (good) points.

- Review_Title: title of the review.

- Review: main content of the review.


<hr/>
<h3>Project made by Valentín Amat.</h3>
<h3>Contact:</h3>

<a href="https://www.linkedin.com/in/valentinamat">LinkedIn</a>  
<a href="https://github.com/ValentinAmat">GitHub</a>  
Mail me at: amatgil5@gmail.com