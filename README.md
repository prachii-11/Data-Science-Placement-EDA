# Data Collection

I collected this data set from Kaggle website. The datasets is related to Data science related placement records of year 2022. The data set have following columns:

1 - Company Name

2 - Job Title

3 - Salaries Reported

4 - Location

5 - Salary

The data set have 2279 rows and 5 columns.

link to the data base repository is: https://www.kaggle.com/code/iamsouravbanerjee/analytics-industry-salaries/data?select=Salary+Dataset.csv

# Exploratory data analysis and handling missing values

Firstly, I checked the data type of all columns to check that wheather data is in correct format or not. After finding that the data is in correct format I take the basic mathematical description of the data using .describe() function. next step was checking and handling missing values. we found 3 missing values in company name column and 2 missing values in salaries reported column that we replace with 'Not available' and 0 respectively.

# Data cleaning

The salary is non generalized and it is in different currency units and also in different time format so we have to bring it in similar currency and in similar time format in order to do our analysis. So, firstly we read the last 3 letters of the salary column in order to get time formats available and found that the salaries is available in /yr, /mo and /hr format then we remove numerical digits and commas from salaries column then we strip last 3 digits of the salaries column in order to get currency symbols available. we found that the dataset have '₹', '$', '£' and 'AFN ' currency symbols in it. Then we remove every symbol, comma and time format from salaries column and type cast it into float object in order to do mathematical calculations on it. then we defined a function that take salary and time format symbol as its input and then convert every salary in /yr format using elif conditional operators. further we define another function that take salary and currency symbol as its input and then convert every salary in indian rupees. Then we map both the functions to the numerical salaries column. Now since we have normalized the salary column in Rupees per year then we can drop all other unwanted columns. Finally using the symbol of currency given we map out that which company pay in what currency.

# Data visualization

Now after cleaning data we tried to answer some basic questions and visually answered it using matplotlib bar graph.

# Data cleaning using MS Excel

We also clean the data in similar way using excel also in order to try and understand both tools for data preprocessing. We use functions like RIGHT() and IFS() functions to achieve similar results then we create a table for entering conversion factors for currencies so that we can change those values using this table which will update new values in main table. We also make sheets for some basic questions like highest salaries offered or highest opportunities available in a Job title, etc. and answered those using data visualization tools of MS Excel.

# Creating Interactive tableau dashboard

Finally we create an interactive tableau dashboard through which we can see quick visualizations and draw insights from it. we use this cleaned data and create dashboards that plots graphs and we can control the variables on the axis of those graphs using drop down controllers and we can also control top numbers shown in the graph using a slider controls. These controls are made using simple case when then statements.Then we finally deployed this dashboard in tableau public so that everyone can access this dashboard using web. link to the dashboard is: https://public.tableau.com/views/datascienceplacements/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link
