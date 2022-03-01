# time-series-data-set-per-hrs-
weather conditions
import pandas as pd

data = pd.read_csv(r"C:\Users\dell\Downloads\weather.csv")

data

# head


data.head()

# shape

data.shape

# index

data.index

# columns

data.columns

# dtypes

data.dtypes

# unique()

data.unique()

# nunique() 

data.nunique()

# count() show the number of null values

data.count()

#  value_counts show unique value in each columns

data['Data.Wind.Speed'].value_count()

# info ()

data.info()

# find the unique wind speed

data.head()

data['Data.Wind.Speed'].nunique()

data['Data.Wind.Speed'].unique()

# number of times wind speed is 4

data.head()

#filttering method
data['Data.Wind.Speed'] == 4.33

data[data['Data.Wind.Speed'] == 4.33]

# null value in the data

data.isnull()

data.isnull().sum()

# rename a column(Date.Month) to month

data.head()

#chnage temperaly
data.rename(columns = {'Date.Month':'month'})

# CHANGE COMPLETLY


data.rename (columns = {'Date.Month':'month'}, inplace = True)

# mean value( month)

data.head()

data.month.mean()

# standard deviation of "Data.Wind.Speed" in data

data.Data.Wind.Speed_kpa.std()

# variance in"Data.Wind.Speed"

data['Data.Wind.Speed'].var

data.head()


#  find all instances when Data.Temperature.Max Temp is above 38 and Data.Temperature.Min Temp is 29

data[(data{'Data.Temperature.Max Temp'}>38) &(data['Data.Temperature.Min Temp'] == 29)]

# max and min value 

data.head()

data.groupby('Data.Temperature.Max Temp').min()

data.groupby('Data.Temperature.Max Temp').max()

# show all the records where Data.Wind.Direction is 17

data[data['Data.Temperature.Avg Temp'] == '39']

