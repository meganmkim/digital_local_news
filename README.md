# Digital Local News for Underserved Communities

## Title ##
**Digital Local News**

## Overview Page ##
--

## Short description of what you aimed to accomplish ##
I listed out the following goals for this project:
1. Increase my comfort level analyzing data using pandas. My first project was more linear and mainly followed the lessons and homework. 
2. Try using a new graphing tool other than Datawrapper. Interested particularly in using D3.
3. Create a new type of graph that was not a pie, line, scatter, etc.
4. Use Figma to customize graph and export into HTML (use figma2html).

## Short description of your findings ##
**Graph 1: Digital Local News in last 10 years**
* Last 10 years is when post of the digital local news organizations that serve underserved communities were founded
* Most of them are founded by advertising, foundation grants, and donors which indicates that the non-advertising organizations still need to seek more sustainable revenues for the long-term
* Most recently founded organizations do not rely on advertising which supports previous research that this previously common source of revenue is potentially not viable

**Graph 2: Revenue Source & Distribution**
* 3 main sources of revenue: advertising, institution funding (grants, corporation, foundations), and individual gifts
* 3 main distribution methods: website, social media, and third-party content platforms
* Strong connection between revenue source and distribution method, but unclear if funders are more inclined to fund these types of local news organizations that distribute with these media types or if these media types have proven some success which draw the funders. It also may be lower cost to build out compared to a mobile app, television, podcast, etc. 


## Summary of the data collection process, with links ##
**Main Data Source:** [Project News Oasis](https://www.projectnewsoasis.com/publications)

## Overview of the data analysis process ##
Data Analysis Process:
1. Project News Oasis offers various filters, but to start, I downloaded the cvs for the entire database for digital native local news publishers to start. The goal was to familiarize myself with all of the categories (columns) and get a general sense of the patterns in the following topics: tax status, year founded, and budget distribution.
2. As I was analyzing the budget distribution, I realized that a significant number of papers were missing: 696 papers did not report on their budget distribution. Only 267 papers had data on this. At this point, I decided to narrow down the filter to groups that likely self-reported in the Project News Oasis survey. I based this on the column category that identifies whether the news organization serves any underrepresented groups (e.g. LGBTQ, ethnic communities, low-income). 
3. I imported a new csv file that contained 98 organizations based on the criteria mentioned above. I checked to see how many data points were missing for the Budget breakdown, and only 7 of them were missing data points.
4. I cleaned up the data columns using .replace(), and then calculated the mean percentage budget breakdown between the 4 categories; editorial, revenue generation, product/technology, and administration. Once calculated, I exported the data frame for a potential data visualization, but ultimately it was not used.
5. The goal was to understand the largest revenue stream and its relationship with distribution methods. To do this, I listed out all of the possible values. I decided to recategorize the values of the revenue stream to 4-5 broader themes so that I could do a data visualization in the form of a sankey.
6. The categorization looked like the following: 
Original dataframe list:
Direct sold advertising                               91
Foundation funding                                    49
Philanthropic funding from major institutions         29
Major individual gifts                                25
Small individual gifts                                21
Grants                                                14
Reader membership                                     11
Events                                                 8
Programmatic advertising                               7
Reader subscriptions                                   5
Other Marketing Services                               4
Haven’t generated revenue yet, but intend to do so     3
Other forms of corporate sponsorship                   3
Syndicated Content                                     2

Recategorization
Individual gifts : Small individual gifts , Major individual gifts 
Advertising : Direct sold advertising , Programmatic advertising, 
Philanthropic Funding: Foundation funding, Philanthropic funding from major institutions, Grants
Reader-Driven: Reader membership , Reader subscriptions  
Other: Syndicated Content , Other Marketing Services, Other forms of corporate sponsorship, Events, 
None: Haven’t generated revenue yet


7. After determining the recategorization, I transformed the values to their new categories and created a new data frame. 
8. I had to clean up the Distribution methods to remove additional spaces. Then I grouped the data frame by distribution to count the main form of revenue stream for each type, and exported this new data frame to use it for data visualization.

## A section about what new skills, approaches, etc you used, or where you grew the most during the project ##
1. Cleaning data using pandas
2. Explored other resources for creating a sankey graph, including a Google template. 
3. Used Figma to annotate the google template sankey and a RAWGraphs Sankey. The Google template, while more simple to hard code my findings into the code, was more difficult to annotate in Figma to do the fragmented components. RAWGraphs was A LOT easier to annotate, but it may also have been because it was my second time around.


## A section about things you tried to do or wanted to do but did not have the skills/time (but if you have more time you might do) ##
1. I wanted to use D3 to create my graphs, but the code was much too difficult to use. I would love to be able to use this tool if I had more time.
2. My second graph, the beeswarm, was a lot simpler. I didn't clean the data very much. Ideally, I would have been able to find a second data source for non-digital local news and compared their revenue sources and founding date to the digital version. A comparison to understand how the funding differs for digital vs. print would have been more insightful, but I didn't have the time for all of those steps. Or, it would be helpful to add in further insight on which orgs are non-profit vs. LLCs.
3. I wanted to apply web scraping to this project, but this database didn't require this and would have overextended me. My main focus was to build upon my previous pandas skills, clean data, and explore new ways to build graphs and annotate using Figma.