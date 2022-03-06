# Power-BI

# Problem Statement 
1.	To track the KPIs of a 40-member team
2.	Parameters
a.	OTD: On Time Delivery
b.	FTR: First Time Right
c.	Effort Variance
d.	Revenue
e.	Revenue per Team Member


# Approach
•	An excel based tracker built and was shared with each team member
•	The excel tracked the following
o	Tasks (with a bill rate and location linked to it)
o	Delivery Date
o	Efforts in terms of hours/day
o	Employee Details
•	The Power BI file pulled data from all these excel sheets stored in a cloud location
•	The data was cleaned and modelled in a Star Schema
•	The report was built with intuitive visual and was used by the management the performance of the project and its members

# Data Transformation 
•	The file locations are parametrized
•	Correct data types are used in each column to facilitate better compression
•	Date table was created in Power Query to ensure better performance
o	Calendar Table
•	Non-Functional Columns were removed to reduce data size
•	“Column Quality” was used to check for errors
•	Dimensional and fact tables are segregated in folders 

# Data Modelling
•	Star Schema implemented
•	Many to Many relationships are avoided
•	Cross filtering is avoided
•	Inactive relationships are used using DAX
•	Unused tables are hidden
•	Columns within a table are grouped into a folder

 
                                              Data Model
 
Folder Structure

# DAX
•	Variables are implemented to reduce the query time
•	DAX is formatted using a website from SQLBI daxformatter.com
•	Important DAX used
o	PARALLELPERIOD()
o	USERELATIONSHIP()
o	FILTER()
o	SELECTEDVALUE()
o	DIVIDE()
o	COMBINEVALUES()
o	CALCULATETABLE()
o	LOOKUPVALUE()
•	Legitimacy of ‘complex’ measures were checked using matrix first
 
                                         DAX Formatting 
