# Hybrid Recommendation System
<img src="https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Images/web.jpg" width="700" height="280"/>
<br/>

<img alt="Website" src="https://img.shields.io/website?url=https%3A%2F%2Fsmhxrecommendersystemapp.herokuapp.com%2F"><img alt="GitHub" src="https://img.shields.io/github/license/SyedMuhammadHamza/Hybrid-recommendation-system-web-application"><img alt="Website" src="https://img.shields.io/badge/Powered%20by-Heroku%20-%236567a5"><img alt="GitHub" src="https://img.shields.io/badge/contributions-welcome-brightgreen"> 

The Regression-based Movie Recommender system that's a hybrid of content-based and collaborative filtering Recommender system. Simply rate some movies and get immediate recommendations tailored for you

## Table of contents
- [Demo](#demo)
- [Live Applicaiton](#live-applicaiton)
- [Accompanying Medium articles](#Accompanying-Medium-articles)
- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Roadmap](#roadmap)
- [Roadmap Step Notebooks](#roadmap-step-notebooks)
- [About Hybrid Algorithm](#about-hybrid-algorithm)
  * [Step 1. Collaborative filtering](#step-1-collaborative-filtering)
  * [Step 2. Content-based filtering](#step-2-content-based-filtering)
  * [Step 3. Prediction](#step-3-prediction)
- [Usage](#usage)
- [Contributing](#contributing)
- [Contact](#contact)
- [License](#license)
- [References](#references)

## Demo
<img src="https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Images/Animation.gif" width="500" height="220"/>

## Live Applicaiton
* [Deployed live application here](https://smhxrecommendersystemapp.herokuapp.com/)

## Accompanying Medium articles
* [Hybrid Recommendation System Web-Application Part 1: Exploratory Data Analysis with PostgreSQL](https://medium.com/@syedmuhammadhamza_23687/hybrid-recommendation-system-web-application-part-1-exploratory-data-analysis-with-postgresql-642ed890c06b)

## Prerequisites
The following open source packages are used in this project:
* Numpy
* Pandas
* Matplotlib
* Flask
* IMDbPY API

## Project Structure 
```
project
│   README.md
│    
└───Data
│   │   Data_README.txt
│
└───Images
|   |   img1.png
|   |   img1.png
|   |   ...
|
└───Model
│   │   Exploratory data analysis with PostgreSQL.ipynb
│   │   Hybrid recommendation algorithm.ipynb
│   │   PostgreSQL_Database_wrapper.py
│   │   Movies_Datase.pkl
│   │   Movies_Learned_Features.pkl
│   │
│   └───images
│       │   img1.png
│       │   img2.png
│       │   ...
│   
└───Server
      │   README.txt
      └───templates
      │     │    home.html
      │     │    layout.html
      │     │    result.html
      └───app.py
      └───Movies_Datase.pkl
      └───Movies_Learned_Features.pkl
      └───requirements.txt
      └───templates
```
## Dataset 
The dataset is provided by GroupLens and can be downloaded from here it contains the following files(links.csv, movies.csv, ratings.csv, and tags.csv)

> "This dataset (ml-latest-small) describes 5-star rating and free-text tagging activity from MovieLens, a movie recommendation service. It contains 100836 ratings and      3683 tag applications across 9742 movies. These data were created by 610 users between March 29, 1996, and September 24, 2018. This dataset was generated on September    26, 2018."

* This [Dataset](https://files.grouplens.org/datasets/movielens/ml-latest-small.zip) of 1 MB is the one used in all Notebooks 
* This [Dataset](https://files.grouplens.org/datasets/movielens/ml-latest.zip) of 265 MB is the one used for training deployed model. 

## Roadmap
This Image sums it All up.
<img src="https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Images/roadmap.jpeg"/>
## Notebook for each step in Roadmap
* [Exploratory Data Analysis(EDA) with PostgreSQ](https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Model/Exploratory%20data%20analysis%20with%20PostgreSQL.ipynb)
* [Feature engineering](https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Model/Hybrid%20recommendation%20algorithm.ipynb)
* [Model building and training](https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Model/Hybrid%20recommendation%20algorithm.ipynb)
* [Model Evaluation](https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Model/Hybrid%20recommendation%20algorithm.ipynb)
* [Deployment](https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Server/app.py)


## About Hybrid Algorithm 
The hybrid recommendation system consists of the following sequence of steps [NOTEBOOK](https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Model/Hybrid%20recommendation%20algorithm.ipynb)
### Step 1. Collaborative filtering
The main objective of collaborative filtering at this step is to learn features for different movies. The implementation of Collaborative filtering here performs "Feature learning" Using a variation of multivariate regression with gradient descent as an optimization algorithm, it takes as input user-item interaction matrix and simultaneously learns both the parameters for different users and features for different movies 
<img src="https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Images/step1.jpg" width="600" height="400"/>

### Step 2. Content-based filtering
The content-based filtering here again is going to be an extension of multivariate regression but unlike collaborative filtering here I'm going to use the features for movies learned using collaborative filtering now to learn online web-application user parameter using content-based filtering thats unique to the user based on his/her web application movie ratings.

<img src="https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Images/step2.jpg" width="600" height="300"/>

### Step 3. Prediction
Prediction (uses both the Features for movies learned using collaborative filtering and the Parameters unique to user learned using content-based filtering to recommend top-N recommendation) The prediction uses both the vectors for movies learned using collaborative filtering and the parameter unique to user learned using content-based filtering to recommend top-N recommendation

<img src="https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/Images/step3.jpg" width="600" height="300"/>

## Usage
Setup to run on localhost<br/>
1. Clone the repository
```
git clone https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application.git
cd ~/Hybrid-recommendation-system-web-application
```
2. Create a Python 3.7 environment.
```
  virtualenv .
```
3. Activate Your Virtual Environment for Linux
```
source bin/activate
```
3. for Windows
```
cd Scripts
then
activate
```
4. Install dependencies.
```
   pip install -r requirements.txt
```
5. Run following command from the directory you have stored the file
```
python app.py
```
## Contributing
Your contributions are always welcome! Contribute by opening an [issue]() or a [pull request](https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application). [Guide](https://github.com/firstcontributions/first-contributions) for beginners to make their first contribution.

## Contact
Any questions can be directed to [syedmuhammadhamza.smh@gmail.com](https://syedmuhammadhamza.github.io/Hamza_Portfolio/)

## License
©SyedMuhammadHamza Licensed under [MIT License](https://github.com/SyedMuhammadHamza/Hybrid-recommendation-system-web-application/blob/main/LICENSE)

## References 
[1]. [H. Zhang, F. Min, D. Ślęzak and B. Shi, "Cost-sensitive regression-based recommender system," 2015 International Conference on Machine Learning and Cybernetics (ICMLC), 2015, pp. 253-258, doi: 10.1109/ICMLC.2015.7340931.](https://ieeexplore.ieee.org/document/7340931)
<br/>
[2]. [G. Lekakos and P. Caravelas, "A hybrid approach for movie recommendation", Multimedia tools and applications, vol. 36, no. 1–2, pp. 55-70, 2008.
updting soon]()
<br/>
[3]. [P. Cremonesi, R. Turrin and F. Airoldi, "Hybrid algorithms for recommending new items", Proceedings of the 2nd International Workshop on Information Heterogeneity and Fusion in Recommender Systems, pp. 33-40, 2011.](https://dl.acm.org/doi/10.1145/2039320.2039325)
