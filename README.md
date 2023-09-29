<br/>
<p align="center">
  <a href="https://github.com/erkutkoral/elev8-Capstone-Project">
    <img src="https://surgesocial.com/wp-content/uploads/2020/03/yelp-home-page.jpg" alt="Logo" width="600" height="400">
  </a>

  <h3 align="center">elev8 Capstone Projectt</h3>

  <p align="center">
    Customer Reviews Analytics with Yelp Data
    <br/>
    <br/>
    <a href="https://github.com/erkutkoral/elev8-Capstone-Project"><strong>Explore the docs »</strong></a>
    <br/>
    <br/>
    <a href="https://github.com/erkutkoral/elev8-Capstone-Project/issues">Report Bug</a>
    .
    <a href="https://github.com/erkutkoral/elev8-Capstone-Project/issues">Request Feature</a>
  </p>
</p>

![Contributors](https://img.shields.io/github/contributors/erkutkoral/elev8-Capstone-Project?color=dark-green) ![Issues](https://img.shields.io/github/issues/erkutkoral/elev8-Capstone-Project) 

## Table Of Contents

* [About the Project](#about-the-project)
* [Technologies-Libraries-Frameworks](#technologies-libraries-frameworks)
* [Roadmap](#roadmap)
* [Authors](#authors)

## About The Project

- Yelp is an application that offers a place for users to post reviews and rate products. According to a study, an increase of one star resulted in a 59% rise in income for small eateries. As a result, we believe that the Yelp dataset has enormous promise as a source of insightful data.

For example:
The main goal of this project is to thoroughly analyze 7 different restaurant cuisine types— Korean, Japanese, Chinese, Vietnamese, Thai, French, and Italian—find out what makes a good restaurant and what customers care about, and then suggest improvements for the future in order to increase revenue. In your role as a Data Scientist, you will mostly evaluate customer reviews to determine why they like or dislike the restaurant. For instance, positive reviews could be the main reason. For example, there may be great reviews primarily due to the friendly service, or negative reviews about high price. Meanwhile, you will also compare among those 7 different cuisine types and figure out differences from reviews and gain valuable insights to make customized recommendations to different types of restaurants.

- Dataset:
  The Yelp dataset is downloaded from Kaggle website. In total, there are 5,200,000 user reviews, information on 174,000 business. you will focus on two tables which are business table and review table.
  • business_id: ID of the business
  • name: name of the business
  • neighborhood
  • address: address of the business
  • city: city of the business
  • state: state of the business
  • postal_code: postal code of the business
  • latitude: latitude of the business
  • longitude: longitude of the business
  • stars: average rating of the business
  • review_count: number of reviews received
  • is_open: 1 if the business is open, 0 therwise
  • categories: multiple categories of the business
  
Attributes of review table are as following:
  • review_id: ID of the review
  • user_id: ID of the user
  • business_id: ID of the business
  • stars: ratings of the business
  • date: review date
  • text: review from the user
  • useful: number of users who vote a review as usefull
  • funny: number of users who vote a review as funny
  • cool: number of users who vote a review as cool
  
## Technologies-Libraries-Frameworks
- Azure Data Lake Gen2 Storage: Data storage and organization.
- Azure Synapse Analytics: Data transformation and warehousing.
- Azure SQL Database: Creating live storage for connection to PowerBI.
- Azure Blob Storage: Cloud-based data storage for files and objects.
- Python: Scripting and data manipulation with Pyspark, Numpy, Pandas, Scikit-Learn libraries.
- SQL: Creating and manipulating tables.
- PowerBI: Data visualization and business intelligence tool.

## Roadmap

1. Uploading Raw JSON data files to Azure Synapse Analytics, Data Lake Storage Gen2.
2. Loading Data files in Azure Notebook with PySpark.
3. Data Understanding, Data Cleaning, Exploratory Data Analysis.
   - In business table, there are 2 columns with missing values and all dataset got no duplicated values.
   - In review table, there are no missing and duplicated values.
   - Filtered out all restaurants of US.
   - Filtered out 50 states of US.
   - Labeled restaurants above rating of 4 as positive, below rating 3 labeled as negative, labeled rating 3 as neural.
   - Dropped rows with neural label.
   - Merged 2 tables with business_id column.
5. Creating Azure SQL Database resource and creating tables within.
6. Uploading Clean Data to Azure SQL Database.
7. Using clean data to understand word patterns by using SVM model.
   - Adjusted the frequencies of various words appeared in each review as features and conducted SVM model to get score of each word.
   - Adjusted 'polarity score'(a value that reflects the polarity of sentiment) towards each restaurant category, the sentiment score of each word was first multiplied by its frequency then normalized by the total number of reviews for the specific category of restaurants.
9. Importing clean data to PowerBI tool for making visualizations.
10. Evaluating insights.
    - When we checked all cuisines, we see that delicious word is the most common top positive word among all cuisines. From there we can say that taste is the top concern in the restaurant businesses. In Japanese, Chinese and Vietnamese cuisines second best concern is freshness of foods that was expected but in the Korean and Thai cuisines being friendly coming earlier than freshness that was unexpected for the Far East cuisine. In French cuisine looks like exaggerated words are used more compare to other cuisines.
    - The reason of high score in French cuisine type is related to the romantic and beautiful appearence or environment.While French restaurants received positive reviews for their sweet food, sweet food is the reason for Korean restaurants to have negative reviews.

## Authors

* **Erkut Koral** - *Industrial Engineer Student* - [LınkedIn](https://www.linkedin.com/in/erkutkoral/)
