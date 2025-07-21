# Impact of Climate Change on Agriculture

**Impact of Climate Change on Agriculture** is a project that seeks to deliver data driven insights to farmers adapting to the ongoing climate crisis.

# ![Banner Image](images/agriculture-climate-banner.jpg)

### Navigation:
* [Data Cleaning](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/jupyter_notebooks/data-cleaning.ipynb)
* [EDA Visualisations in Python](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/jupyter_notebooks/data-visualisations.ipynb)
* [Statistical Analysis](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/jupyter_notebooks/statistical-analysis.ipynb)
* [Tableau Dashboard](https://public.tableau.com/app/profile/jane.weightman/viz/climate-change-agriculture/MainStory?publish=yes)
* [Raw Data](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/data/climate-agriculture.csv)
* [Clean Data](https://github.com/Janeweightman/Climate-Change-Impact-on-Agriculture-/blob/main/data/clean-agriculturedata.csv)


## Dataset Content
* The dataset was found on Kaggle and be found [here](https://www.kaggle.com/datasets/waqi786/climate-change-impact-on-agriculture). The dataset contains 10,000 rows and 15 columns. The dataset includes allows for a wide scope of inquiry, including variables on crop yield, CO2 emissions, extreme weather events and more. 


## Business Requirements
* Describe your business requirements


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





* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. From the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.
