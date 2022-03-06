# Problem Statement

- To track the KPIs of a 40-member team
- Parameters
  - OTD: On Time Delivery
  - FTR: First Time Right
  - Effort Variance
  - Revenue
  - Revenue per Team Member

# Approach

- An excel based tracker built and was shared with each team member
- The excel tracked the following
  - Tasks (with a bill rate and location linked to it)
  - Delivery Date
  - Efforts in terms of hours/day
  - Employee Details
- The Power BI file pulled data from all these excel sheets stored in a cloud location
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
- Cross filtering is avoided
- Inactive relationships are used using DAX
- Unused tables are hidden
- Columns within a table are grouped into a folder



                                                                     # Data Model
![alt text](https://github.com/sovanp438/Power-BI/blob/8b040536792c2c0ecb6b19be2481ba79897b1340/Images/Data_Model.png "Logo Title Text 1")

![](RackMultipart20220306-4-bcm388_html_7caef3124d3d3d6f.png)

Folder Structure

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

![](RackMultipart20220306-4-bcm388_html_821da9496e7a72b1.png)

# DAX Formatting
