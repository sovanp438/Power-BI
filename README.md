# Project Management Dashboard

- To track the KPIs of a 40+ member team
- Parameters
  - Timely & Defect-free Delivery
  - Effort Variance
  - Revenue
  - Revenue per Team Member etc.

## Overall KPI

![alt text](https://github.com/sovanp438/Power-BI/blob/30f31e99e5b9b5b9e83dcd599ada3040e60f7db3/Images/Report_1.png "")


## Revenue

![alt text](https://github.com/sovanp438/Power-BI/blob/5b82470980e9186bbc77448563492b81875ecfa2/Images/Report_2.png "")

# Approach

- An excel based tracker was built and shared with each team member
- The excel tracked the following
  - Tasks 
  - Delivery Date
  - Efforts in terms of hours/day
  - Employee Details
  - Bill Rate
  - Location
  - Domain etc.
- The Power BI file pulled data from all these excel sheets stored in a OneDrive Location
- The data was cleaned and modelled in a Star Schema
- The report was built with intuitive visual and was used by the management the performance of the project and its members

# Data Transformation

- The file locations are parametrized
- Correct data types are used in each column to facilitate better compression
- Date table was created in Power Query to ensure better performance
  - [Calendar Table](https://radacad.com/all-in-one-script-to-create-calendar-table-or-date-dimension-using-dax-in-power-bi)
- Non-Functional Columns were removed to reduce data size
- &quot;Column Quality&quot; was used to check for errors
- Dimensional and fact tables are segregated in folders

# Data Modelling

- Star Schema implemented
- Many to Many relationships are avoided
- Cross filter both direction is avoided
- Inactive relationships are used using DAX
- Unused tables are hidden
- Columns within a table are grouped into a folder



                                                              Data Model
                                                              ----------
![alt text](https://github.com/sovanp438/Power-BI/blob/8b040536792c2c0ecb6b19be2481ba79897b1340/Images/Data_Model.png "Logo Title Text 1")





                                                           Folder Structure
                                                           ----------------
![alt text](https://github.com/sovanp438/Power-BI/blob/6408d8d628536ed062e4e8abb995c478dce8bb14/Images/Folder_Structure.png "")


# DAX

- Variables are implemented to reduce the query time
- DAX is formatted using a website from SQLBI daxformatter.com
- Important DAX used
  - PARALLELPERIOD()
  - USERELATIONSHIP()
  - FILTER()
  - SELECTEDVALUE()
  - DIVIDE()
  - COMBINEVALUES()
  - CALCULATETABLE()
  - LOOKUPVALUE()
- Legitimacy of &#39;complex&#39; measures were checked using matrix first



                                                          DAX Formatting
                                                         ----------------
![alt text](https://github.com/sovanp438/Power-BI/blob/6408d8d628536ed062e4e8abb995c478dce8bb14/Images/DAX%20Formatting.png "")
