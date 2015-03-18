# 1989zhao.github.io

This .tex shows mainly three parts of my visualisation establishment. Part.1 illustrates the process for hosting a copy of my visualisation. Part.2 describes the figures of my website(also shows on the explanation parts of the website). Part.3 shows 5 types of data error. Additionally, the link for website hosting is: 

 http://1989zhao.github.io


Part.1
(1).create website repository with the name 1989zhao.github.io, ensure it is public and initialise it with a README as shown below.
(2). Click the settings option ---> github pagessection--> automatic page generator--> publish button-->generate http://your-username.github.io

Part.2 These visualisations show the experience in terms of schedule and cost planning to the government and investment organisations for Education Project future planning. Additionally, they also show the achievement in Education Project to citizens:
1. Cost Analysis
(1).This visualisation compares the LifecycleCost, PlannedCost($M) and ProjectedCost($M) for the 50 education projects, which shows whether most of the actual cost of Education Projects meets the planned budget. In order to enable investment organisations and government to plan the future budget for education project development. 

(2).These three kinds of cost are mainly range from 0.1($M) to 10 ($M). However,it also shows clear that the LifecycleCost for ProjectID 1368 is 25654.96 which not only much lager than PlannedCost 5837.8985,but also has a large gap with other peer projects. And ProjectID 1349 and 1353 also shows this problem, the LifecycleCost of ID.1349 is 136.24 and ID.1353 is 23.237, these two projects are much larger than the Planned and Projected cost and other projects. (3).Additionally, project 1352 cost extremely lower than other projects, but it met planed and projected cost.

(3). Trancing graph shows that the previous education projects are planned well, because mostly of the actuarial cost met the planned cost, but the comparison of these three cost shows that usually the lifecycle cost is higher.  

2.Schedule (Date) Analysis
(1). This visualisation shows the Date issues of the Education Project for the investment organisations and government to visual the general duration of the education project to support the future schedule plan for the education project, and this shows that education projects usually finished within 2-3 years.
(2). There are 2 points clearly show errors:
    ProjectID 2860: the completion date is Sep/2017 however the projected date is Sep/2012, thus it is clear that the the completion year should be changed to 2012.
    ProjectID 1368: the started date is Sep/2007, however the started date for others are mostly range from 2010 to 2012, hence this stared date shows error.
 (4).The fitting visualisation shows that mostly of these education project are for the year 2011 to 2013. There are only 2 projects started in 2009, basically the date shows no significant errors but when look into it, it is clear that ProjectID 1618 and 1617 lost for 5 years and 4years separately and without Planed time and Projected time, although it shows no clearly errors in data. However, when look the the Planned Date and the Projected Date it can be seen that the Project with the name of of “New Award Year Release” and “Research and Development Environment” both missing the Planed Date and the Projected Date.

Part.3 Dataset errors: 

(1). mixed data formats

go to column for date: then text facet- select text facet.then quick scroll the panel and then in column completion data: the first date is 2012-30-09, different from others time descriptions, should change to 30/09/2012. this invalid date affects 1 records./ 

(2).multiple representations

go to “Agency name”: edit cells - common transforms—trim leading and trailing whitespace then cluster “Department of Agriculture” together

go to the “Agency Name”: edit cells- cluster and edit，

Cluster “FileNET P8 Platform” with “FileNet P8 Platform” under fingerprint
Cluster “First Half-Year” with “First-Half Year”  under “ngram-fingerprint”
I also can directly edit “Agriculture Department” in text facet

but DoA,DoE, DoJ, DoT, DoD cannot do in this way

 “DoE” cab both be “Department of Energy” and “Department of Education”, looking the content it is education department and “the Department” cannot be modified in this way, is contents 2 agency code, should be edit further

(3).summation records
go to the “Business ID”: text facet- “Total” rows(178), and these summaries don’t spoil the later processing and delete with “ALL” —Edit rows- Remove all matching rows


(4).mixed use of numerical scales
go to “lifecycle cost”:numerical facet—change-add .log(), compare error ones the “planed cost”. than the “Project ID” 1941,its “lifecycle cost” is “242.985 ($m)” much bigger than the “Planned Cost” “11.442”,should be changed 

(5). Redundant Data 

the Project ID and Project Name represent same thing, add them together in a new column to represent the Project(the project ID is number but can separate the project from each other, project names repeat each other), vita text: value+”(“ +cells[”ProjectID”].value+”)”, then the column show both of their information and distinguish Projects from each other for visualisation. And the Agency Name and Agency ID also combine together.


Part.4 Exceptional
Based on the visualisation,  there are 2 exceptional part should be added to the dataset. One part is one type of cost which is not included in the projected cost should be added, because the lifecycle cost generally more than the projected cost, hence, an additional cost must be exist. The other part is the  



