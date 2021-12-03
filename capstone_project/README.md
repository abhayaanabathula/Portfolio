### Overview

The term data science was coined as recently as 2008 when companies realized they needed data professionals who could organize and analyze massive amounts of data. Successful data scientists are able to identify relevant questions, collect data from a multitude of different data sources, organize the information, translate the results into solutions, and effectively communicate the findings in a way that postively affects decisions. The life cycle of a data scientist consists of acquiring data, cleaning, modeling, making predictions, and then giving recommendations ([*source*](https: //ischoolonline. berkeley. edu/data-science/what-is-data-science/)). 

---

### Problem Statement

As with any job, the salary will always vary. Salaries can vary based on location, the job level/ position, the responsibilities entailed, and so on. Especially for those just entering the job field or market, it can be really hard to tell a company what you think they should pay you. Job search engines show that salary can range from 87-130 thousand but that’s just the based on state; salary will definitely be different based on the company and projects. There’s such a broad range of skills and so many different types of work a data scientist can do you could be working on, it can be a hard and overwhelming process. The goal of this project was to create models that accurately predict the average salary of a job based on experience, the job description, the job title, location, and key skills. Addtionally, those predictions would be utilized by an interactive application where an individual can input their specific job skills and other meaningful key words and be given a salary estimate. This estimate could be used in interviews to ensure fairness to all parties ([*source*](https: //www. ziprecruiter. com/Salaries/ What-Is-the- Average-Data-Scientist-Salary-by-State)). 

From Kaggle Challenge ([*source*](https://www.kaggle.com/ankitkalauni/predict-the-data-scientists-salary-in-india))

---

### Datasets

* [`Final_Test_Dataset.csv`](datasets/Final_Test_Dataset.csv): test dataset provided by Kaggle challenge   
* [`Final_Train_Dataset.csv`](/datasets/Final_Train_Dataset.csv): train dataset provided by Kaggle challenge
* [`citypop.csv`](/datasets/citypop.csv): dataframe of cities in India with population ([*source*](https://worldpopulationreview.com/countries/cities/india))
* [`train_cleaned.csv`](/datasets/train_cleaned.csv): final clean of train data   
* [`train_first_clean.csv`](/datasets/train_first_clean.csv): first cleaning and data reformatting
* [`quantified_data.csv`](/datasets/quantified_data.csv): dataset of quantitative dataset with count vectorized string data   

---

### Data Dictionary

|Feature|Type|Description|
|---|---|---|
|experience|Object|Range of experience required in years|
|job_description|Object|Description of job, responsibilities/ entailments|
|job_desig|Object|The job designation/ title|
|job_type|Object|Job sector|
|key_skills|Object|List of key skills such as management, sql, java, etc.|
|location|Object|Location of the job|
|salary_range|Object|The salary range of the given job in rupees|

---

### Analysis

For the quantitative variable analysis, the models did not perform well; the Random Forest Regressor performed the best with an accuracy score of 0.47. NLP analysis performed very poorly. The KNeighbors Regressor performed the best with a score of 0.22, but the train and test scores suggest overfitting. Finally, analysis with all the variables included produced poor results as well. The AdaBoost Regressor performed the best with a score of 0.38, but again this model was overfit. The models were not given much in terms of inputs for analysis. The manipulations and reformatting might’ve masked interactions between the variables. A potential solution could have been to maybe create a list of features with all possible experience years and have the label also be a list of all possible salary estimates. Gridearching with other parameters should have also been done. The main issues seem to lie within the dataset itself. All the variables were recorded as string objects, including the experience and salary variables. The poor results make sense given how drastically the variables were changed and changing the datatypes as well. Dealing with this dataset was definitely not an exact science and so these results were expected.

 
---

### Conclusions/Recommendations 

There were a lot of problems with the dataset created from combining the count vectorized data with the other quantitative data to be used for analysis. For one, it took forever for the dataframe to be created and then trying to save it to the machine kept causing the notebook to time out. In order to combat this, I attempted to create the dataset in google colab. The dataframe was created, but now all the available RAM was being used when simply trying to read in that newly created dataframe. To fix this, I decided to create the dataset and run the models all within the same workbook, but again the session was running out of RAM and kept crashing. Eventually, sampling the data along with accounting for indices allowed for the models to run. The issue with this is I had to use a small chunk of the dataset, which could have affected the results. There were also a lot of issues when trying to actually push the project to github. The terminal kept throwing an error when trying to push the large csv file created. A recommended solution was to create a gitignore file and then ignore all csv files. This is good practice for data allocation, for as long as the links to the datasets are added hard copies of the csv files do not need to be included. Additionally, other datasets created within the code would be created and saved to the reviewing persons machine regardless. In order to remove the large files from the staging area, I ran git reset soft. The project was then able to be successfully pushed. 

The next steps for this project would potentially be to look into other data formats. One data format is pickle, which is a way to stream data. A pickle module is used to serialize objects. Serializing objects means to convert the object into a stream of bytes to store the object or transmit it to memory. Another data format is parquet, which stores the data in columns (csv files store data in rows). Additionally, pandas has full support for parquet files. Feathers are a data format where dataframes are pushed in and out of memory as efficiently as possible. Another avenue would be to look into relational databases. Relational databases provide a way of storing and accessing very large datasets. The data would be stored on the disk and then can be progressively loaded in batches and then queried using SQL. Another option could be databricks. The last resort for this project would be to use AWS. All in all, I need to figure out a way to manage these large data files for analysis ([*source*](https://machinelearningmastery.com/large-data-files-machine-learning/)).

Stretch goals for this project include creating an interactive web application and webscraping data from job searching webpages to be used for analysis. Additionally, I am looking to apply this same logic to other job sectors. 
