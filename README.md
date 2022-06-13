# interactive_dashboard_CNN_news
## Summary

The goal of this project is to analyze [previously collected data](https://github.com/vollenia/web_scraper-CNN_news) from the the CNN (Cable News Network) website for the year of 2021. While the [previously performed analysis](https://github.com/vollenia/data_analysis_CNN_news) delivered plots that could only be presented as a static image, this project is aimed at creating interactive plots and bundeling them together into a dashboard that can be viewed and interacted with in the browser.

Once again, the focus of this analysis lies not on the contents of the articles themselves but on the meta information of these articles and since there is no specific problem that needs to be solved, an exploratory analysis is performed. For this purpose the data has been re-collected on the 2<sup>nd</sup> of May, 2022 and reflects the state of the CNN website at this point in time, which deviates slightly from the state reflected [_previously_](https://github.com/vollenia/data_analysis_CNN_news).

The analysis is performed in Python 3.10.3 and presented in a Jupyter notebook format. The virtual environment needed to run the notebook can be re-created by using the included _requirements.txt_.
To view the interactve dashboard, navigate to the root directory of the repository and run _panel serve interactive_dashboard.ipynb_ from within the virtual environment.

## Analysis of the Year

## Analysis of the Months

## Dashboard
The dashboard consists of two main pages where the first page displyas the _Year_ view and the second the _Months_ view with their corresponding plots. The user can switch freely between the two pages using the widget located under _Settings_ in the sidebar.

- VIDEO BOTH PAGES (MAIN WIDGET)

While the _Year_ view consists of the three discribed plots, the _Months_ view allowes for displaying the same three plots for each of the individual months. The months can be navigated through the widget located at the top of the _Months_ page.

- VIDEO MONTHS PAGE (MONTHS WIDGET)

The dashboard is designed to adapt to different browser settings and will resize accordingly. If resizing manually, the page might need to be reloaded to be displayed properly.
