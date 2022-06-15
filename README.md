# interactive_dashboard_CNN_news
## Summary

The goal of this project is to analyze [previously collected data](https://github.com/vollenia/web_scraper-CNN_news) from the the CNN (Cable News Network) website for the year of 2021. While the [previously performed analysis](https://github.com/vollenia/data_analysis_CNN_news) delivered plots that could only be presented as a static image, this project is aimed at creating interactive plots and bundeling them together into a dashboard that can be viewed and interacted with in the browser.

Once again, the focus of this analysis lies not on the contents of the articles themselves but on the meta information of these articles and since there is no specific problem that needs to be solved, an exploratory analysis is performed. For this purpose the data has been re-collected on the 2<sup>nd</sup> of May, 2022 and reflects the state of the CNN website at this point in time, which deviates slightly from the state reflected [_previously_](https://github.com/vollenia/data_analysis_CNN_news).

The analysis is performed in Python 3.10.3 and presented in a Jupyter notebook format. The virtual environment needed to run the notebook can be re-created by using the included _requirements.txt_.
To view the interactve dashboard, navigate to the root directory of the repository and run _panel serve interactive_dashboard.ipynb_ from within the virtual environment.

## Analysis of the Year
This chapter focuses on the analysis of the year as a whole. It contains plots that visualize the progression of publications, distribution of authorship and a table that represents the year as a single workweek. The idea is to get an initial objective impression of the data that will provide not only valuable insights but also allow to develop an intuition as to which aspects to inspect further.

### Publications Throughout the Year
When we inspect the progression of the publications throughout the year as one continuous line, we observe a significant degree of fluctuation in the number of publications. To get a clearer understanding of this fluctuation, we use polynomial regression to create the yellow trend line which smooths out the harshness of the blue line resembling the raw publication counts. The green line on the other hand visualizes the continuous delelopment of publication counts and is created by performing linear regression. Despite the high fluctuation, we observe a significant increase in publications throughout the year.

Having made the plots interactive, enables us not only to inspect any point along any of the lines but also to blend out individual lines. This becomes very useful when we intend to tell a story about the data to an audience since we can then do this gradually, instead of overloading our audience with multiple overlapping curves.

- VIDEO YEAR LINE

### Distribution of Authorship
While knowing the progression of publications, we don't know how these publications came to be. Therefore, we need to inspect their authorship. Considering the large number of journalists working for CNN, we don't want to look at every single one individually but group them together in a reasonable manner. The approach selected, consist of mainly distinguishing between a single contributor to the contents of the article and a collaboration between multiple authors. Additionally, articles which don't provide any name author are included as a separate group.

Inspecting the chart, we observe that roughly 11% of atricles don't contain any named author and individual contributions and collaborations resemble a roughly 2 to 1 relationship. This provides us with the insight that for most day-to-day news articles, the work of one single journalist is sufficient.

- VIDEO PIE YEAR

### Year as a Workweek
Instead of viewing each day individually, the reporting on news can be consided a recurring "workweek" event throughout the year. 
Contrary to the mostly common five day workweek, news atricles are being published seven days a week, resulting in a workweek from Monday to Sunday. To inspect the contribution of individual weekdays to the overall picture, we condense the information from the whole year into a one week representation.

Viewing the total _Counts_, we see a significant dropoff towards the weekend, which is also reflected in the _Median_ values with a 30% decrease for Saturday and 40% for Sunday. Observing the _Standard Deviation_ we further see a notably lower degree of fluctuation for the weekend, ulimately indicating that not only are less articles being published on the weekends but that this is happening consistently.

- VIDEO TABLE


## Analysis of the Months
This chapter focuses on the analysis of the individual months. It contains plots that visualize the distribution of authorship, progression of publications as well as the density of dublications for each month contrasted against the whole year. While the plots for the year as a whole show a broad picture, the idea here is to be able to inspect individual components that make up this broad picture in more detail.

### Distribution of Authorship
Same as the analysis of authorship over the whole year, the data from each month is grouped into three classes (single, collaboration, unknown). While displaying these resuls in form of a pie chart would likely be a better fit, the overarching focus on the synergy between all plots for the monthly view required the use of a different type of visualization.

- VIDEO BAR AUTHORSHIP

### Publications Throughout the Month
In this context, the publications of individual days are represented as bars which display furter information when interacted with.
The interaction is triggered uppon a vertival overlap of the cursor with the positions of the individual bars, resulting in triggering the bars annotations by simply moving the cursor horizonatally across the plot. This appears to be a reasonable implementation given the horizonally stretched nature of the plot and the absence of overlapping lines.

- VIDEO BAR MONTH PUBLICATIONS

### Density of Publications
When viewing the density of publications for each month, we have the opportunity to view it in context of the density graph for the whole year. This is possible because we are viewing the distriburion within each month and therefore, individual variations, such as the varying number of days between each month or even between a month and the whole year, don't play a role.

As for interactivity. It is possible to blend out ether the density for the year or the density for the displayed month.

- VIDEO DENSITY MONTH

## Dashboard
The dashboard consists of two main pages where the first page displyas the _Year_ view and the second the _Months_ view with their corresponding plots. The user can switch freely between the two pages using the widget located under _Settings_ in the sidebar.

- VIDEO BOTH PAGES (MAIN WIDGET)

While the _Year_ view consists of the three discribed plots, the _Months_ view allowes for displaying the same three plots for each of the individual months. The months can be navigated through the widget located at the top of the _Months_ page.

- VIDEO MONTHS PAGE (MONTHS WIDGET)

The dashboard is designed to adapt to different browser settings and will resize accordingly. If resizing manually, the page might need to be reloaded to be displayed properly.
