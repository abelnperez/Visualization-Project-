
#  | Extract, Transform, Load (ETL) Project ✂🗄🛢

![](https://github.com/abelnperez/Extract-Transform-Load-ETL-Project/blob/main/images/etl-diagram.png)

## Main goal ♻♻♻ 

The objective of this project is to do the complete ETL (Extract, Transform, Load) with two conditions, it is mandatory to use 2 extraction methods and to obtain the data from three different sources. 

The extraction methods have been through an API and a CSV:

   - **API**: the spanish electric red https://www.ree.es/en/apidatos
   - **CSV**: 2 CSV files from 2 diferent sources

The sources are:

   - **API**:  https://www.ree.es/en/apidatos
   - **Kaggle**: https://www.kaggle.com/datasets/mannmann2/world-per-capita-energy-consumption/
   - **Our World in Data**: https://ourworldindata.org/energy


## Extraction  🕹

We have done analytical research from different websites to understand the electric market since a new company has the will to enter the Spanish energy sector in the renewables category. After our research we have found some relevant information, one data set about the World Per Capita Energy Consumption, a second one about the World Energy Consumption, and also the Spanish Electric Net API. 

## Transformation  🕹

In the first URL, we got the first DataFrame, we carefully cleaned it and obtained the relevant information for our project. We deleted the columns with no relevant information and simplified the DataFrame getting only the information from the countries that belong to the European Union to do a future comparison between them. From the second data frame, we got more relevant information, especially the kinds of energy, the source of the energy, the energy per capita, and more. It was also necessary to create more columns with relevant metrics for the project like the total_fossil_energy, total_renewable_energy, renewable_energy_percentage, and fossil_energy_percentage. With that information on hand, we decided to jump into the Spanish Electric Net API to know how much of the energy is obtained from fossil resources and how much is obtained from renewable sources. We got into the API and we extracted the relevant information that we needed, unfortunately, the information stored there just reached 2016. 


## Load  🕹

Once the transformation data was completed we got 3 DataFrames that we converted into dictionaries to export into MongoDB, where we created the energy database and the collection. We did the exportation and completed the load process.

![](https://github.com/abelnperez/Extract-Transform-Load-ETL-Project/blob/main/images/dataframe.PNG)

## Information  🎞🕹

The repository is divided in the following files:

- **Folder data:**

   - **raw data**: raw csv´s.
   - **clean data**: csv´s after cleaning.

- **Folder notebooks:**

   - **cleaning_API_REE.ipynb**: this file is the API information cleaned.
   - **cleaning_per_capita_energy.ipynb**: the file where the per capita energy informatio is stored.
   - **Cleaning_WEC.ipynb**: this is the file where the world energy consumption data are gathered. 

- **Folder images:**
   - the folder to save memes and graphs.
   


## Links & Resources 📂 📂 📂 

[Pandas](https://pandas.pydata.org/docs/)

[Numpy](https://numpy.org/doc/1.18/)

[Python](https://docs.python.org/3/library/functions.html)

[Python Functional Programming](https://docs.python.org/3.7/howto/functional.html)

[Data Cleaning with Numpy and Pandas](https://realpython.com/python-data-cleaning-numpy-pandas/#python-data-cleaning-recap-and-resources)

[MongoDB Compass](https://www.mongodb.com/)

