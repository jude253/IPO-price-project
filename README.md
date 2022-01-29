# IPO-price-project

This project is going to be a web page that shows the price change from IPO companies' intial price to their current price.  
I am using the [finnhub.io](https://finnhub.io/) free API for now to make a front end.  In order to run this page in the 
browser with data from finnhub.io, you will need to sign up for a free account then paste in your API token on [this line in
index.html](https://github.com/jude253/IPO-price-project/blob/35a682ac35391b75df423b83a29afd7d34910558/index.html#L27).


## Note on Data Sourcing
This webpage is in its infancy, and because of the API limit of 60 requests/minute and the fact that there are 200+ IPOs in a 
year, I believe the best way to populate this page will be to have an SQL database that updates the data for all IPOs in 
the past 5 years once a day or month at a rate of around 60 companies per minute, then we can query that data from this webpage
without any limits on how many companies we can load per minute.  We can even do all of the math with SQL and only have 1 query
to populate all of the pages data.  However, this approach means that we will need to make a backend and our data on a company's
current will not be the current price in this moment in time, only from the last refresh of the SQL database.
