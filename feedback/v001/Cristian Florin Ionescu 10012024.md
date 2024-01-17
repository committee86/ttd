Time To Data Framework 

## Comments by Cristian Florin Ionescu on Jan 10, 2024

Hi, Andrei, I am glad to see this framework being fleshed out. Here are a few additions and contributions:

1. Tasks are not equal - yes! Totally agree on this point, this ties very well back to what I call “Strategic Analytics Adoption”. This is the framework that I use to ensure that the data analytics infrastructure that we put in place directly addresses and supports the company’s main initiatives. The way this would apply to your framework is: assign priorities to the requirements. If the data request ties back to an important annual goal such as decreasing inventory, then it should have priority 1 and a 100% weight. If it is more of a nice to have incremental improvement type of request, then it should have a priority 3 and TTD should be diluted to a 33% weights. TTD 1 of 15 days + TTD 3 of 30 days = 15 * 100% + 30*33% / 2 requests = 12.5 days. Let me know how you like that.

2. Secondly, Time to Data as a KPI should be comprised of multiple sub KPIs. Since a request is coming until the relevant data is used, we go through several stages:
 - is the required data identified
 - does it reside in a source system from where we can pull it automatically at the right level of granularity and refresh frequency?
 - is the data already available in a database and can be readily used?
 - does it adhere to data governance and data quality standards?
 - is the refresh properly monitored through logs and alerts?
 - does the user have a way to access and consume it? (API, web interface, etc)
 - does the data have proper metadata and documentation, is it indexed and discoverable?

I think here we need a decision tree:
 - do we know what data we need? If yes, then: is the data available in a system? If yes, then, do we have a programmatic interface to access it? If no, send to data engineering to create the data source. If yes, then is it monitored and is the quality assured? If yes, then, etc

As such, I would then break TTD into sub KPIs: time to search and identify + time to create the data set (data engineering) + time to get access to it + time to perform QA + etc. I’ll leave the heavy lifting to you to further document the necessary steps.

Please note that the decision tree I am proposing takes into account both data availability and access considerations as well as data quality considerations.

3. And finally, I have a simple proposal to compute the KPI. Task management tools allows you to create a pipeline with predefined stages and stage owners. Also, any ticket movement from one stage to the other is recorded and accessible through an API. So, my proposal is, use a tool like Hubspot, define the stages, monitor the tickets and then compute the relevant visualization funnel.

Having an aggregated funnel would not only allow measuring TTD, but also break it down by request type or business line. Some scenarios:
 - if we see multiple data requests related to supply chain data taking too long - this is a sign we need a curated data warehouse with supply chain data readily available, indexed and searchable.
 - is data engineer John taking too long to create datasets? If yes, let’s put in place a learning and development plan for him to increase his skills so he can ship data assets faster.
 - are data assets requests waiting too long because the data is not correct? Then, let’s put in place a task force to ensure that all the critical ETLs that are powering the most essential data are properly monitored, logged and have the right alerts going to the persons accountable to maintain accuracy.

I hope my comment will help you further refine this concept. I love what you did so far!
