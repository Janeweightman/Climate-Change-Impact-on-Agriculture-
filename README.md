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
* The dataset was found on Kaggle and be found [here](https://www.kaggle.com/datasets/waqi786/climate-change-impact-on-agriculture). The dataset contains 10,000 rows and 15 columns. The dataset includes allows for a wide scope of inquiry, including variables on crop yield, CO2 emissions, extreme weather events and more. 


## Business Requirements
* The business goal of this project is to provide information to farmers, governments and policy makers on how they can best adapt to climate change 
* This is a very important problem to address as according to Christine Li et al in [Nature](https://www.nature.com/articles/s41598-025-87047-y) countries in sub-Saharan Africa, North America, South Asia and Oceania could be at risk of failing to meet national calorie demands by the end of the centuary. 
* We seek to identify trends in the data that can help farmers feed the planet and maximise their profit in a sustainable way. 


## Hypothesis and how to validate?
* List here your project hypothesis(es) and how you envision validating it (them) 

## Project Plan
To help plan we used a github project planning board which can be found [here](https://github.com/users/Janeweightman/projects/5).
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
No private data is in this dataset, however there are still ethical considerations. 
There are very view observable trends in the data, including no trends regarding anthropogenic causes of climate change. Readers should not interpret the results of this study to engage in climate change denialism, the data is completely synthetic and does not reflect the very real dangers of climate change.

## Dashboard Design
The dashboard can be found [here](https://public.tableau.com/app/profile/jane.weightman/viz/climate-change-agriculture/MainStory?publish=yes).
### Formatting 
Tableau's story format was used to give an intuitive structure to the dashboard, with questions on each section of the story to add intrigue. The grey colour format was chosen to be easy on the eyes and not draw attention away from the data.
![Dashboard story format](images/storyboardformat.png)
As you can see the dashboard is split into 4 sections, answering 4 different questions.

### Dashboard page 1: 
![Page 1 Dashboard](images/Page1dashboard.png)
The first page of the dahsboard answer the question whether soil health has an economic impact. The figure is scatter plot with an added trend line. 
We have added the option to filter by both country and crop type using tick boxes on the right hand side.

### Dashboard page 2:
![Page 2 Dashboard](images/page2dashboard.png) 
Page 2 answers the question of whether greater crop yields result in an economic boom. The graph is a scatter plot with a trend line, allowing the viewer to see the trend clearly. We have added the option to filter by Crop Type, as well as Year in the form of a slider that allows the user to specify a specific time period for example 2014-2020.


### Dashboard page 3:
![Page 3 Dashboard](images/page3dashboard.png)
Page 3 seeks to answer 2 questions; the first one being whether different adaptation strategies effect crop yield and the second being whether different adaptation strategies have an economic impact. Both questions are answered with bar charts placed one on top of the other for easy comparison. The bar charts are sorted in ascending order and coloured according to adaption method, allowing the viewer to compare the differences between charts, for example the viewer can more easily see that 'Organic Farming' is better than 'Water Management' for crop yields in the first chart.  We have included options to filter by crop type and country on the right hand side, as well as a legend for the adaptation methods. 

### Dashboard page 4: 
![Page 4 Dashboard](images/page4dashboard.png)
Page 4 of the dashboard examines CO2 Emissions and temperature over time, it uses a dual axis line chat with corresponding trend lines. The lines are colour codes with a legend and the chart features filters for country and crop type. 
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
we added an explanation of the R-Squared value to page 2 of the dashboard for the benefit of the non technical audience. 

![Textbox R-Squared](images/textboxrsquared.png)


## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

## Development Roadmap
* We had issues with converting year to date/time data type, we decided to keep it as a 64 bit integer, this caused no problems.
* In previous projects we had issues with images not showing when put into a folder, this has been fixed during this project demonstrating growth. 
* There have been a number of times when code did not run, this was fixed with a combination of rubberducking and debugging with Co-Pilot. 
* A major issue was with the dataset itself, the data shows very little trends. When choosing the dataset we read the high usability score and assumed this wouldn't be an issue. In the future when choosing a Kaggle dataset we will make sure to look at the comments and previous projects to ensure you can tell a compelling story. 
 


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 


### Media

- Header image was made using [Canva](https://www.canva.com/)
- Random Forest diagram image can be found [here](https://miro.medium.com/v2/resize:fit:720/format:webp/1*ZFuMI_HrI3jt2Wlay73IUQ.png)


## Acknowledgements (optional)
* Thank the people who provided support through this project.
