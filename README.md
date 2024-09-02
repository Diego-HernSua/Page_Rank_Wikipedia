# Page Rank (Massive Computing)
This project involves the creation and implementation of the PageRank algorithm utilizing Apache Spark within the Databricks environment. The focus is on efficiently computing the ranking of web pages based on link structures obtained from Wikipedia

## Understanding PageRank
PageRank is a fundamental algorithm used by search engines like Google to determine the importance of web pages. Developed by Larry Page, one of Google’s founders, it calculates a ranking for each web page based on its link structure. The more important the pages linking to a given page, the higher its PageRank.
The algorithm begins by assigning an initial rank to each page. This rank is then distributed across all the links that the page points to. The process repeats iteratively, with each page's rank being recalculated based on the ranks of the pages linking to it. Over multiple iterations, the ranks stabilize, giving a final measure of each page’s importance.

## Implementation Overview
To implement the PageRank algorithm, we start by exploring the Wikipedia dataset, focusing on key fields like "title," "id," and "text." The next step is to extract links from the text content of each page, which allows us to understand the connections between different pages.

We then create a forward links table that maps each page to its outbound links, followed by a backward links table that records the incoming links for each page. These tables are crucial for calculating the PageRank, as they define the network of connections.

The PageRank algorithm is applied in two main phases. First, we set up the initial conditions, including defining a damping factor, setting a maximum number of iterations, and assigning initial PageRank values. Then, the algorithm is iterated until the ranks converge or the maximum number of iterations is reached. Finally, we output the ranked list of pages, providing insights into the relative importance of each page in the network.
