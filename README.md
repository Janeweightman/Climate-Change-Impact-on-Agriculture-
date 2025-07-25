# Impact of Climate Change on Agriculture

**Impact of Climate Change on Agriculture** is a project that seeks to deliver data driven insights to farmers adapting to the ongoing climate crisis.

# ![Banner Image](images/agriculture-climate-banner.jpg)

### Navigation:
* [Data Cleaning](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/jupyter_notebooks/data-cleaning.ipynb)
* [EDA Visualisations in Python](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/jupyter_notebooks/data-visualisations.ipynb)
* [Statistical Analysis](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/jupyter_notebooks/statistical-analysis.ipynb)
* [Tableau Dashboard](https://public.tableau.com/app/profile/jane.weightman/viz/climate-change-agriculture/MainStory?publish=yes)
* [Machine Learning](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/jupyter_notebooks/machinelearning.ipynb)
* [Raw Data](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/data/climate-agriculture.csv)
* [Clean Data](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/data/clean-agriculturedata.csv)


## Dataset Content
* The dataset was found on Kaggle and be found [here](https://www.kaggle.com/datasets/waqi786/climate-change-impact-on-agriculture). The dataset contains 10,000 rows and 15 columns. The dataset allows for a wide scope of inquiry, including variables on crop yield, CO2 emissions, extreme weather events and more. 


## Business Requirements
* The business goal of this project is to provide information to farmers, governments and policy makers on how they can best adapt to climate change.
* This is a very important problem to address as according to Christine Li et al in [Nature](https://www.nature.com/articles/s41598-025-87047-y), countries in sub-Saharan Africa, North America, South Asia and Oceania could be at risk of failing to meet national calorie demands by the end of the century. 
* We seek to identify trends in the data that can help farmers feed the planet and maximise their profit in a sustainable way. 


## Hypothesis testing 
### H1: Soil Health Drives Economic Productivity
* We hypothesised that soil health would be a major driver behind economic productivity.
* We first tested the distribution of the variables using density distribution plots to determine the appropriate statistical tests to apply. 
#### Distribution for Soil Health:
![soil health density](images/densityofsoilhealth.png)

As you can see the distribution of soil health is not normally distributed, and infact it has a distinctive uniform distribution, this means it is suitable for non parametric tests. 

#### Distribution for Economic Impact: 
![Economic Impact Distribution](image.png)

As you can see the distribution is skewed towards lower values meaning it is also suitable for non parametric statistical tests. 
#### Spearman Rank Correlation
![H1 Spearman Rank](images/h1spearman.png)

We conducted a Spearman Rank Correlation test, the results were decisive with a correlation coefficient of -0.009 there is no monotonic relationship, and with a P-Value of 0.410 the results were not statistically significant. We thus have to reject our alternative hypothesis and accept the null hypothesis that soil health does not drive economic impact.

#### Graphing H1: 
![h1 graph](images/page1ofdashboard.png)

As you can see there is no correlation, however if you remember the distribution graphs from perviously you can see that pattern playing out in the above figure. Notice how the triangles become less dense on the Y axis but remain dense on the X axis, this is because soil health is a uniform distribution and economic impact is skewed towards lower values.
### H2: Crop Yields Boost Economic Growth
* We predict that greater crop yields will result in an economic boom
* First we need to check the distribution of crop yields using a density plot
#### Distribution for Crop Yields
![Density of crop yields](images/cropyielddistribution.png)

Crop yields are not normally distributed making them suitable for non parametric tests.
#### Spearman Rank Correlation
![h2 spearman](images/h2spearman.png)

With correlation coefficient of 0.735 and P-value well below 0.05 we can say there there is both a monotonic relationship and that it is highly stastistically significant. Thus we can accept our alternative hypothesis. 
#### Graphing H2
![h2graph](images/h2graph.png)

As you can see there is a clear corrrelation and the R Squared value is 0.515 which means that this linear regression explains 51.5% of the economic impact. 
#### Machine Learning model to test H2 
* we used a random forest decision tree to test actual vs predictied values. The model can be found [here](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/jupyter_notebooks/machinelearning.ipynb).

![Random Forest diagram](images/randomforest.webp)

The above figure is from this [article](https://miro.medium.com/v2/resize:fit:720/format:webp/1*ZFuMI_HrI3jt2Wlay73IUQ.png).

![ML results](images/mlresults.png)

We consulted with co-pilot to explain the results to help us tell a story with this ML model. The R squared score means that 46.7% of economic impact can be explained by crop yield alone, which means it's a very significant factor, although less significant than the Tableau linear regression displayed earlier. The RMSE (Root Mean Squared Error) value means that on average the model is $295 million dollars off the actual values. This model is helpful as it shows us how impactful crop yields are to economic growth, furthermore a model like this one or similar could be used to make forecasts for future economic growth.

### H3: Different adaptation strategies have a more positive impact on crop yield
* We pedict the adaptation strategy farmers choose have an impact on overall crop yield.
#### Kruskal-Wallace H test
Since adaptation stategy is a nominal variable Kuskall-Wallace H test was chosen. 

![h3 kruskal](images/h3kruskal.png)

With H-statistic of 3.407 and p-value of of 0.492 we can determine that different adaptation strategies not not have significant impact on crop yields. We therefore have to accept the null hypothesis.

#### Graphing H3:
![graph h3](images/graphh3.png)

As you can see there is very little difference between adaptation strategies, even no adaptation is more successful than organic farming or water management. 

### H4: different adaptation strategies have more positive impacts on the economy

* We predict that some of the adaptation strategies farmers choose will have a more positive impact on the economy.

#### Kruskal-Wallace H test:
![h4 kruskall](images/h4kruskal.png)

With an H-statistic of 5.760 and p-value of 0.218 there is no significant impact of adaptation strategies on economy. We therefore have to accept the null hypothesis. 

#### Graphing H4: 
![h4 graphing](images/h4graphing.png)

This is a very similar graph to the previous hypothesis, demonstrating that adaptation strategy does not have an economic impact. 

### H5: CO2 emissions are correlated with temperature
One of the fundamentals of anthropogenic climate change is that man made CO2 emissions are causing a rise in global temperatures. 
* First we need to see the distributions of the variables
#### Distribution of CO2 Emissions
![Density of CO2 Emissions](images/densityofco2.png)
 
The CO2 Emissions have a non normal uniform distribution, making it suitable for non parametric tests 

#### Distribution of Temperature 
![Temp density](images/tempdensity.png)

Temperature is not normally distributed and has a uniform distribution, suggesting non parametric tests would be suitable. 

#### Spearman Rank Correlation
![H5 Spearman](images/h5spearman.png)

With a Spearman correlation of 0.004 and p-value of 0.719 we can reject the alternative hypothesis. 

#### Graphing H5 over time
The link between these factors might be more apparent if we plot them across time.

![H5 Graph](images/h5graph.png)
From the graph we can see that there might be some link between the two variables although further analysis would be necessary to be sure. 


## Project Plan

To help plan we used a github project planning board which can be found [here](https://github.com/users/Janeweightman/projects/5). The project board gave a structured approach to planning that allowed us to identify the steps and the priority that we should give them.

![project plan](images/projectplan.png)

Within the tasks in the project plan we used tick boxes so we can tick off tasks as we complete them. 

 ![tickboxes](images/tickboxes.png)

* To ideate hypotheses we used a mixture of EDA, literature review and bouncing off ideas with Co-pilot. 
* Data was collected from Kaggle, processed in jupyter notebook, analysed using statistical tests in python and intepreted using a mix of literature review and generative AI.


## The rationale to map the business requirements to the Data Visualisations
* 1: The first visualisation is a scatter plot looking at soil health and economic impact, this meets the business requirements as one of the main goals of the project is for famers to find out how to maximise their profit sustainably. 
* 2: The second visulaisation is a scatterplot looking at economic impact of crop yield, this also tries demonstrate how to maximise profit. 
* 3: The third and fourth visualisations are both bar charts that compare adapatation strategies against economic impact and crop yield. This allows farmers to make an informed business decision on what adaptation stategy to choose based on their economic return and crop yield. 
* 4: The fifth visuaslisation is a line chart plotting CO2 and temperature across time.This meets the business requirements as farmers cand gain insight into the general trend of climate change and how important it is to take action. 

## Analysis techniques used
* Data cleaning in pandas using a Jupyter Notebook gave a structured modular approach that allows both data practioner and reader to follow each step.
* EDA visualisations in Python also allows a modular easy to follow approach to data exploration and the range of visualisation libraries available makes for aesthetically pleasing visualisations. One issue with this however is that Plotly visualisations are not viewable on github repositories, which means some level of technical competancy is required from the reader to fork the repo. An alternative sollution could be to do visualisations in R using ggplot2, this is a method we would love to explore in future projects. 
* Dashboard visualisations were made in Tablaeu Public, this for us was the best way to do it as it allows for a pre built story format and aesthetically pleasing visualisations. Another pro of Tablaeu over another software such as PowerBI is that it is incredibly easy to share your Dashboard using just a link. 
* Generative AI specifically Co-pilot was used for hypothesis ideation, code debugging, code generation and storytelling. 
* Scikit-Learn was used for machine learning as it's relatively easy to use library for machine learning tasks. 
* Sci-py was used for statistical tests as it allows for a wide range of both parametric and non parametric tests. 
* Git was used for version control.


## Ethical considerations
No private data is in this dataset, however there are still ethical considerations. 
There are very view observable trends in the data, including no trends regarding anthropogenic causes of climate change. Readers should not interpret the results of this study to engage in climate change denialism, the data is completely synthetic and does not reflect the very real dangers of climate change.

## Dashboard Design
**The dashboard can be found [here](https://public.tableau.com/app/profile/jane.weightman/viz/climate-change-agriculture/MainStory?publish=yes)**.
### Formatting 
**Tableau's story format** was used to give an intuitive structure to the dashboard, with questions on each section of the story to add intrigue. The grey colour format was chosen to be easy on the eyes and not draw attention away from the data.
![Dashboard story format](images/storyboardformat.png)
As you can see the dashboard is split into 4 sections, answering 4 different questions.

### Dashboard page 1: 
![page 1 dashboard](images/page1ofdashboard.png)
**The first page** of the dahsboard answer the question whether soil health has an economic impact. The figure is scatter plot with an added trend line. 
We have added the option to filter by both country and crop type using tick boxes on the right hand side.

### Dashboard page 2:
![Page 2 Dashboard](images/h2graph.png) 
**Page 2** answers the question of whether greater crop yields result in an economic boom. The graph is a scatter plot with a trend line, allowing the viewer to see the trend clearly. We have added the option to filter by Crop Type, as well as Year in the form of a slider that allows the user to specify a specific time period for example 2014-2020.


### Dashboard page 3:
![Page 3 Dashboard](images/page3dashboard.png)
**Page 3** seeks to answer 2 questions; the first one being whether different adaptation strategies effect crop yield and the second being whether different adaptation strategies have an economic impact. Both questions are answered with bar charts placed one on top of the other for easy comparison. The bar charts are sorted in ascending order and coloured according to adaptation method, allowing the viewer to compare the differences between charts, for example the viewer can more easily see that 'Organic Farming' is better than 'Water Management' for crop yields in the first chart.  We have included options to filter by crop type and country on the right hand side, as well as a legend for the adaptation methods. 

### Dashboard page 4: 
![Page 4 Dashboard](images/page4dashboard.png)
**Page 4** of the dashboard examines CO2 Emissions and temperature over time, it uses a dual axis line chat with corresponding trend lines. The lines are colour coded with a legend and the chart features filters for country and crop type. 
* **Please note that page 4 does feature a lot of white space beneath the diagram, this is an intentional trade off between aesthetics and functionality as that white space does become occupied if you change the filters.** 
![changing the filters on dashboard](images/changingfilters.png)
### How the dashboard communicates to technical and non-technical audiences.
A good example of a feature that both informs the technical and non-technical audiences is the trend lines. For a non-technical audience the trend line gives a visual cue to identify trends in data, however for a technical audience it comes with a tooltip that tells you the R squared value and P-value.
![trend line tooltip](images/tooltip.png)

#### Filters enable further analysis and engagement through interactivity
![Filters](images/filters.png)

### Adding Median to dashboard page 2
We later decided to add more useful information regarding the median values of crop yields and economic impact to the dashboard. We caculated this using median lines in the graph. We use median rather than mean as we know they are no normally distributed.

![Median Crop Yield](images/mediancropyield.png)

![Median Economic Impact](images/medianeconomicimpact.png)

This did not look aesthetically pleasing, so we took the calculations, removed the lines and added a text box to the story. 

![Median Text Box](images/mediantextbox.png)

### Adding explanation of R Squared to Dashboard page 2:
we added an explanation of the R-Squared value to page 2 of the dashboard for the benefit of the non-technical audience. 

![Textbox R-Squared](images/textboxrsquared.png)

## Development Roadmap
* We had issues with converting year to date/time data type, we decided to keep it as a 64 bit integer, this caused no problems.
* In previous projects we had issues with images not showing when put into a folder, this has been fixed during this project demonstrating growth. 
* There have been a number of times when code did not run, this was fixed with a combination of rubberducking and debugging with Co-Pilot. 
* Ploty was problematic and required a pip install of nb format 4.2.0, which is why 4.2.0 exists as a file in the Jupyter notebook folder.
* A major issue was with the dataset itself, the data shows very little trends. When choosing the dataset we read the high usability score and assumed this wouldn't be an issue. In the future when choosing a Kaggle dataset we will make sure to look at the comments and previous projects to ensure you can tell a compelling story. 
* We realised we are heavily reliant on generative AI for building machine learning models, in the future we plan to hone our skills in building ML pipelines with less assistance from AI.
 


## Main Data Analysis Libraries
* **Pandas**: Pandas was used throughout the course as it allows the manipulation of data frames.
* **Matplotlib**: Matplotlib was used to make EDA visualisations.
* **Plotly**: Plotly was used to make EDA visualisations.
* **Seaborn**: Seaborn was used to make EDA visualisations.
* **SciPy** SciPy was used for statistical tests.
* **Scikit-Learn** SkLearn was used for machine learning. 



## Credits 

### literature review resources:
* Infomation on soil health from [yara](https://www.yara.co.uk/grow-the-future/sustainable-farming/soil-health/)
* Information on the 2038 problem from [wikipedia](https://en.wikipedia.org/wiki/Year_2038_problem)
* Information on the imporatance of climate change's impact on Agriculture from [Nature](https://www.nature.com/articles/s41598-025-87047-y) 
* Information on Spearman Correlation from [Statstutor](https://www.statstutor.ac.uk/resources/uploaded/spearmans.pdf)
* Information on Random Forest Regression from [Chaya from Level Up Coding](https://levelup.gitconnected.com/random-forest-regression-209c0f354c84)

### General project resources
* [Microsoft Co-Pilot](https://copilot.microsoft.com/chats/qxDMq9YFBmUafioNYmFnR) was used to aid in code generation, debugging, ideation, story telling and nagivating Tableau. 
* Tutorials from [Tableau Tim](https://www.youtube.com/channel/UC7HYxRWmaNlJux-X7rNLZyw) were used while learning Tableau
* [Code Institute LMS](https://learn.codeinstitute.net/dashboard) modules on Pandas, Numpy, Statistics,python visualisations, Tableau and machine learning were used throughout the project including code re-worked for data cleaning and python visualisations.
* Markdown formatting from [Markdown Guide](https://www.markdownguide.org/basic-syntax/).

### Media

- Header image was made using [Canva](https://www.canva.com/)
- Random Forest diagram image can be found [here](https://miro.medium.com/v2/resize:fit:720/format:webp/1*ZFuMI_HrI3jt2Wlay73IUQ.png)


## Acknowledgements
* A special thanks to all the Tutors at Code Institute!
* I would like to thank Kaori from my previous group project who I took inspiration from when building my dashboard.
* A huge thank you to all  my classmates who provided good conversation and support throughout the course.
