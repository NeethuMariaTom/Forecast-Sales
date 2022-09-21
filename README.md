# Forecast-Sales
A major European drug distributor company operates over 3,000 drug stores across seven European countries. 
Since a lot of drugs come with a short shelf life, that is, they do not have a long expiry date, it becomes imperative for the company to 
accurately forecast sales at their individual stores. Based on the historical data provided for 1115 stores, a forecasting model has 
to be built to forecast the daily sales for the next six weeks. Since the company is just embarking on this project, the scope has been kept to 
nine key stores across Europe. The stores are key for the company keeping in mind the revenue and historical prestige associated with them. 
These stores are numbered - 1,3,8,9,13,25,29,31 and 46.

Data Defenition:
The data is provided in two tables, stores and train.

The store table contains the metadata for every single store including the following:

Store - an Id that represents the store
StoreType - differentiates between 4 different store models: a, b, c, d
Assortment - describes an assortment level: a = basic, b = extra, c = extended
CompetitionDistance - describes thedistance in meters to the nearest competitor store
CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb, May, Aug, Nov" means each round starts in February, May, August, November of any given year for that store
The train table contains the sales data for individual stores at a daily level along with the details about the day

Store - a unique Id for each store
DayOfWeek - Describes the day of the week (1 - Monday till 7 - Sunday)
Date - Describes the date on the day
Sales - the turnover for any given day (this is what you are forecasting)
Customers - the number of customers on a given day
Open - an indicator for whether the store was open: 0 = closed, 1 = open
StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools
