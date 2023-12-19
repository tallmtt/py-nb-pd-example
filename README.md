# Python, Jupyter notebook and Pandas Example
To demonstrate example for Python (py), Pandas (pd), in Jupyter notebook (nb)

Video link:

### Save this code using github

- Make a free account:
- Install git
  - $ sudo apt install git
- cd to your projects folder:
  - For example:
    - $ cd ~/Projects
- $ git clone git@github.com:tallmtt/py-nb-pd-example.git

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
3. Install python libraries for this project (Jupyter notebook and Pandas (also matplotlib for plotting))
   - pip install notebook
   - pip install pandas
   - pip install matplotlib
4. Start up Jupyter notebook with the activated virtual environment in the Project folder
   - $ cd /home/user/Projects/py-nb-pd
   - $ jupyter-notebook
5. Open a browser to continue working
6. To stop - hit Ctl+C in the console

### In Browser:
1. Open a New Notebook (on right side)
2. Rename the file by clicking on the name (Untitled)
3. Start coding
   - For this example - you can open up and walk through my example notebook
     - In each box
       - Pressing Ctl+Enter will run the code but not advance
       - Pressing Alt+Enter will run the code and make a new box underneath
     - I am commenting everything to hopefully be self explanatory

## Notes:

Ways to import files:
- Import csv file
  - df = pd.read_csv("diabetes.csv")
- Importing Excel files (single sheet)
  - df = pd.read_excel('diabetes.xlsx')
- Importing Excel files (multiple sheets) (Extracting the second sheet  since Python uses 0-indexing)
  - df = pd.read_excel('diabetes_multi.xlsx', sheet_name=1)
- Importing JSON file
  - df = pd.read_json("diabetes.json")

Outputting a DataFrame:
- Into a CSV file
  - df.to_csv("diabetes_out.csv", index=False)
- into a JSON file
  - df.to_json("diabetes_out.json")
- into a text file
  - df.to_csv('diabetes_out.txt', header=df.columns, index=None, sep=' ')
- into an Excel file
  - df.to_excel("diabetes_out.xlsx", index=False)

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
| Get the mean of each column value   | df.mean()                 |
| Get the mode of each column value   | df.mode()                 |
| Get the median of each column value | df.median()               |
| Create Pivot Tables                 | pd.pivot_table()          |

## References:
- [Jupyter Notebook](https://jupyter.org/)
- [Pandas](https://pandas.pydata.org/docs/getting_started/index.html)

### Learn More (also where some of this is from)
- [pytoLearn Plots](http://pytolearn.csd.auth.gr/b4-pandas/40/plotserdf.html)
- [Spark by Example](https://sparkbyexamples.com/pandas/how-to-plot-columns-of-pandas-dataframe/)
- [10 Min to Pandas](https://pandas.pydata.org/docs/user_guide/10min.html)
- [w3 schools Pandas Tutorial](https://www.w3schools.com/python/pandas/default.asp)
- [Python Examples Pandas Tutorial and Examples](https://pythonexamples.org/pandas-examples/)
- [Datacamp Pandas](https://www.datacamp.com/tutorial/pandas)
- [Listen Data Pandas](https://www.listendata.com/2017/12/python-pandas-tutorial.html)

### Data Used Here:
- ['income' data](https://raw.githubusercontent.com/deepanshu88/Datasets/master/UploadedFiles/income.csv): This data contains the income of various states from 2002 to 2015. The dataset contains 51 observations and 16 variables.
