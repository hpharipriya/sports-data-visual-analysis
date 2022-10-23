# sports-data-visual-analysis
Last 10 year Cricket match Analysis fir Top 5 ranked Teams

## Description
Sports data is high-dimensional data with multiple magnitudes. Exploring and extracting information from it is interesting, challenging, and of high demand. Adequate visualization techniques are needed to represent these data and to tell a story precisely. In this paper, we are trying to understand the characteristics of sports data using one-day international men’s cricket data and finding out the best visualizations used for analyzing the data. The research is focused on finding the factors affecting a team's victory using visualization techniques. In the background study, we have examined various papers from the generic visualization domain, sports domain, and cricket data visualization reports. All different aspects of this information are combined and used for the whole research.
First, we identified major features from cricket match data and analyzed them using various techniques like regression. With the help of previous papers, applied different visualization techniques used in the field such as heat maps, scatter plots, multiple stacked bar plots, and line charts. Combined more features in the visuals and tried detailed visualizations of the area of interest to do a deep analysis. After creating visuals, the usability evaluation is done using a group of 10 people and made improvements based on feedback.
Web scraping is used for data collection and Spotfire is the visualization tool used for the study.

This study is an attempt to understand the factors affecting the success rate of a team. Team victory is determined by several factors, including the teams’ strong areas, weather, toss, players’ rating, and so on. We are exploring a team’s success rate and its dependency on the above-mentioned features to determine various factors such as a safe score to achieve a win, winning patterns of different teams, individual contribution towards the overall team performance and other factors.
Research Questions
Case 1:
1. What is a typical safe score for a team to win?
2. What is the winning pattern of a team? Chasing the score or batting first?
Case 2:
1. Is there any positive relation between playing in home ground and match win for top 5 teams?
2. Is there any positive relation between toss win and match win for top 5 teams?
3. What are the changing trends over the last 5 years when considering the team's performance, run rate, total score? Does the success rate depend on team rank, run rates?

## Data preparation
The cricket data required various cleaning, grouping, and transformations before the implementation of the visualization model. The ESPNcricinfo website collects and arranges data of every match on their stats page. This develops time- series data for each team with attributes such as match result, ground, team's run rates. Wikipedia pages were used to collect the team ranks over years. There were other data sources too that we tried to extract data from initially. While ESPNcricinfo pages have the feature to filter and group data by team, opposition, year, and results. This we found to be more structured to meet our requirements and include features to answer our research questions. However, the data is available in webpages in HTML format, so we developed a custom web scraping script in NodeJS using cheerio, a tool for parsing HTML and XML in NodeJS and fetched the last 10 years' data for the matches played among top- performing teams. The data obtained was in JSON format and converted into CSV using online tool https://www.convertcsv.com/json-to-csv.htm.


Visualization and interaction
Case1: What is a typical safe score for a team to win?
For the first case, to find a safe score, I have used the scatterplot visual with year and score in x and y-axis respectively. Color is chosen as the tool to distinguish match results and various teams are shown using different shapes. The scatter plot is chosen because there are a limited number of points to show, and it can adapt by adding 4 features to show simultaneously for this case.





