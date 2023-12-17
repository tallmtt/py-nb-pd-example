# Python, Jupyter notebook and Pandas Example
To demonstrate example for Ppython (py), Pandas (pd), in Jupyter notebook (nb)

Video link:

## Install/Learn Procedure:

### In command prompt
1. Install python3
2. Make a virtual environment for this project and activate it
   - This will be **project-specific,** meaning anything installed in this environment is for this project
   - This is considered a best practice as some libraries will conflict so they should not be make systemwide
     - If a system wide tool is desired, use "pipx" (Because I use Jupyter notebook so often for random python things, I do have it installed this was ALSO)
   - How to make a virtual environment:
      - $ python3 -m venv name-of-new-venv
        - I will name this venv "pynbpd"
        - $ python3 -m venv pynbpd
      - Activate the environment by:
        - $ source ./name-of-new-venv/bin/activate
      - To deactivate the environment (when you are done):
        - $ deactivate
3. Install python libraries for this project (Jupyter notebook and Pandas, maybe Numpy in future)
   - pip install notebook
   - pip install pandas
4. Start up Jupyter notebook with the activated virtual environment in the Project folder
   - $ cd /home/user/Projects/py-nb-pd
   - $ jupyter-notebook 
5. Open a browser to continue working

### In Browser:
1. Open a New Notebook (on right side)
2. Rename the file by clicking on the name (Untitled)
3. Start coding
   - For this example - you can open up and walk through my example notebook
     - In each box, hitting Ctl+Enter will run the code but not advance
     - I am commenting everything to hopefully be self explanatory

## Data:
- ['income' data](https://raw.githubusercontent.com/deepanshu88/Datasets/master/UploadedFiles/income.csv): This data contains the income of various states from 2002 to 2015. The dataset contains 51 observations and 16 variables. 

## Notes:

| Utility                             | Functions                 |
|-------------------------------------|---------------------------|
| Extract Column Names                | df.columns                |
| Select first 2 rows                 | df.iloc[:2]               |
| Select first 2 columns              | df.iloc[:,:2]             |
| Select columns by name              | df.loc[:,["col1","col2"]] |
| Select random no. of rows           | df.sample(n = 10)         |
| Select fraction of random rows      | df.sample(frac = 0.2)     |
| Rename the variables                | df.rename( )              |
| Selecting a column as index         | df.set_index( )           |
| Removing rows or columns            | df.drop( )                |
| Sorting values                      | df.sort_values( )         |
| Grouping variables                  | df.groupby( )             |
| Filtering                           | df.query( )               |
| Finding the missing values          | df.isnull( )              |
| Dropping the missing values         | df.dropna( )              |
| Removing the duplicates             | df.drop_duplicates( )     |
| Creating dummies                    | pd.get_dummies( )         |
| Ranking                             | df.rank( )                |
| Cumulative sum                      | df.cumsum( )              |
| Quantiles                           | df.quantile( )            |
| Selecting numeric variables         | df.select_dtypes( )       |
| Concatenating two dataframes        | pd.concat()               |
| Merging on basis of common variable | pd.merge( )               |

## References:
- [Jupyter Notebook](https://jupyter.org/)
- [Pandas](https://pandas.pydata.org/docs/getting_started/index.html)
