# Pandas:
- Pandas is a fast, powerful, flexible and easy to use open source data analysis and manipulation tool,
built on top of the Python programming language.

## [Pandas Notebook](https://github.com/justmarkham/pandas-videos/blob/master/pandas.ipynb)

### How do I read a tabular data file into pandas?
- read_table assumes the data is tab sperated
- Assumes first row is a header row

**Example 1:**
```python
# conventional way to import pandas
import pandas as pd

# read a dataset of Chipotle orders directly from a URL and store the results in a DataFrame
orders = pd.read_table('http://bit.ly/chiporders')

# examine the first 5 rows
orders.head()
```
<img width="736" alt="Screenshot 2023-05-24 at 3 08 31 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/4ffdfea2-1ea0-4ea8-ba41-71c35bbdd81a">


**Example 2:**
```python
import pandas as pd

# read a dataset of movie reviewers (modifying the default parameter values for read_table)
user_cols = ['user_id', 'age', 'gender', 'occupation', 'zip_code']

# sep -> identifies the separator(if data is not properly formatted)
# Header = None -> No header is speified in the data
users = pd.read_table('http://bit.ly/movieusers', sep='|', header=None, names=user_cols)


# examine the first 5 rows
users.head()
```
<img width="317" alt="Screenshot 2023-05-24 at 3 11 50 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/a6ad3ec1-4d33-4bf0-81cb-e64e7a762776">

**Tips:** 
- skiprows=None & skipfooter=0 to skip the data above and below (noramlly place where developer provids notes about the data)

### How do I select a pandas Series from a DataFrame:
```python
import pandas as pd

# read a dataset of UFO reports into a DataFrame
ufo = pd.read_table('http://bit.ly/uforeports', sep=',')

# read_csv is equivalent to read_table, except it assumes a comma separator
ufo = pd.read_csv('http://bit.ly/uforeports')

# examine the first 5 rows
ufo.head()
```
<img width="524" alt="Screenshot 2023-05-24 at 3 25 13 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/1524f4fa-1caa-45c8-9c83-119d61c882cf">

```python
import pandas as pd

# read a dataset of UFO reports into a DataFrame
ufo = pd.read_table('http://bit.ly/uforeports', sep=',')

# read_csv is equivalent to read_table, except it assumes a comma separator
ufo = pd.read_csv('http://bit.ly/uforeports')

# examine the first 5 rows
ufo.head()
```
