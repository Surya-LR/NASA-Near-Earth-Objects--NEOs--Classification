# NASA Near Earth Objects (NEOs) Classification
This project gets Data from NASA API and conducts a supervised learning experiment.
Near-Earth objects (NEOs) are asteroids or comets that orbit the Sun and whose orbits come close to that of
Earth’s. Of the more than 600,000 known asteroids in our Solar System, more than 20,000 are NEOs(The
European Space Agency,2021). The aim of this coursework is to classify, potentially hazardous asteroids and
comets, according to the risk of impacting earth.

## Classfication information:

**The Target Variable**: ‘is_potentially_hazardous_asteroid’

**Target Type**: Logical (TRUE or FALSE)

**Task**: Classification

Inspiration for this coursework came from a personal interest in space exploration programs.

## Data Source:

The dataset was compiled using the NASA Near Earth Object Web Service (NeoWs) which is accessible from
https://api.nasa.gov/ under the heading “Asteroids - NeoWs”.
In order to obtain full access this API, one has to register with NASA and obtain a personalised API key.
The query is limited to a 7-day date range and the number of queries that can be made is limited to 1000
queries per hour.

## The Layout of the two files:

The dataset was extracted from the content part of the JSON object that is received through the API for the
Near Earth Objects (NEOs).
As this API is not accessible using the ‘nasadata’ package, it has to be compiled by calling queries. For this
project, the dataset is going to be compiled for the last two years, using RStudio in ‘Data_API_NASA.rmd’
as shown in figure below.

![image](https://github.com/Surya-LR/NASA-Near-Earth-Objects--Classification/assets/77691667/4ad4d08c-6df4-40cd-bd65-7b60a503557f)


## The classifiers:

The classifiers selected are:

• SVM(poly) with tuning for C, degree and scale

• Random Forest (RF) with tuning for mtry

## Comparison of Outcomes:

Accuracy is not the best metric for comparison in this imbalanced Dataset as it will provide a very high
accuracy even if the minority class is rarely predicted correctly.For this Dataset,the recall is just as important
as precision due to the nature of the classification outcome.

## Sample metric : Confusion Matrix (Random Forest combinations):

![image](https://github.com/Surya-LR/NASA-Near-Earth-Objects--Classification/assets/77691667/a532b73a-196f-4086-9326-368e31dc7bce)

## Best Classifier and Repo combination:

![image](https://github.com/Surya-LR/NASA-Near-Earth-Objects--Classification/assets/77691667/b0a31ac4-9648-4791-a187-bec9ca5ac58b)

