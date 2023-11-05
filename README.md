
#  | Extract, Transform, Load (ETL) Project ✂🗄🛢

![](https://github.com/abelnperez/Extract-Transform-Load-ETL-Project/blob/main/images/etl-diagram.png)

## Main goal ♻♻♻ 

The objective of this project is to do the complete ETL (Extract, Transform, Load) with two conditions, it is mandatory to use 2 extraction methods and to obtain the data from three different sources. 

The extraction methods have been thorough an API and a CSV:

   - **API**: the spanish electric red https://www.ree.es/en/apidatos
   - **CSV**: 2 CSV files from 2 diferent sources

The sources are:

   - **API**:  https://www.ree.es/en/apidatos
   - **Kaggle**: https://www.kaggle.com/datasets/mannmann2/world-per-capita-energy-consumption/
   - **Our World in Data**: https://ourworldindata.org/energy


## Extraction  🕹

We have done an analitical research from different websites to understand the electric market since a new company has the will to enter in the spanish energy sector in the renowables category. After our reserach we have found some relevant information, once data set about the World Per Capita Eenergy Consumption, a second one about the World Energy Consumption, and also the Spanish Electric Net API. 


## Transformation  🕹

In the first url we got the first DataFrame, we carefully cleaned it and obtain the relevant information for our project. We deleted the columns wiht no relevatn information and simplified the DataFrame getting only the information from the countries that belong to the European Union to do a future comparison between them. From the second DataFrame we got more relevant information, specialy the kinds of energy, the source of the energy, the energy per capita and more. It was also necesary to create more columns wiht relevant metrics for the project like the total_fossil_energy, total_renewable_energy, renewable_energy_percentage and the fossil_energy_percentage. With that information on hand we decided to jumpo into the Spanish Electric Net API to know how much of the energy is obtained from fossil resorces and how much is obtained from renewable sources. We got into the API and we extracted the relevant information that we needed, unfortunately the information stored there it just reach until 2016. 


## Load  🕹

Once the transformation data was completed we got 3 DataFrames that we converted into dictionarys to export into MongoDB, where we created the energy data base and the collection. We did the exportation and completed the load process.

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

[Python Functional Progragmming] (https://docs.python.org/3.7/howto/functional.html)

[Data Cleaning with Numpy and Pandas](https://realpython.com/python-data-cleaning-numpy-pandas/#python-data-cleaning-recap-and-resources)

[MongoDB Compass](https://www.mongodb.com/)

