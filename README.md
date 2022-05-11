# stock_price_prediction
Implementing a LSTM.nn to predict the future prices of an equity

![alt_text](Readme-title.png "Title")

# airbnb_london_data_blog

Working with the public **airbnb** data for London at my first project in _Udacity Nanodegree Data Science_ course.

## About Airbnb - and my motivation - _Business Understanding_


Airbnb is a great platform that offers hospitality in a great and different way.
One of the data offered from the Data Science program in Udacity, was the airbnb public data.
My previous experience in real state pushed me to work with this data. It interested me immediately.
I have been always curious about how airbnb works, how big it is, or how profitable could be in London. The possible of dig in this data makes me think that I can answer some of this questions or maybe some other interesting questions, an it did.
Airbnb is a huge company working with thousands of properties and a lot of features, meaning data in great quantities.


## Discovering the Airbnb Data - _Data Understanding_

### The Data:
	
The data we were able to access was the public airbnb data, delivered by the inside airbnb webpage. You can found them in the next link:
	
[www.insideairbnb.com](http://insideairbnb.com)

Or directly to the data page, searching for London data:
	
[inside_airbnb_public_data](http://insideairbnb.com/get-the-data.html).

Look for the London data and download the next files (for size problems we were unable to upload those files into this GitHub):

- listings.csv.gz for **November 2020**
- listings.csv.gz for **October 2019**
- listings.csv.gz for **October 2018**
- listings.csv.gz for **April 2017**
- calendar.csv.gz for **November 2020**
- reviews.csv.gz for **November 2020**

### The file:

The file used to process all the data and its subsequent analysis is a Jupiter-Notebook, python programmed:

udacity-datascience-1stproject-blog-carlosarocha.ipynb

### Libraries:

Please be sure to have already installed in your notebook environment the next libraries:

* numPy
* pandas
* matplotlib
* datetime
* os
* re
* mpl_toolkits
* sklearn


### Change The Initial Paths:

After download the data listed before, you have to change the **paths** placed at the beginning of the code, used to download the data into the 		program.
The next path need to be updated with the new location of the data:

* path_l20
* path_l19
* path_l18
* path_l17
* path_c20
* path_r20

#### My conclusions about the data founded:

The data included in the public airbnb files is very basic. It seems to be exactly the data that anybody can found while searching for a property to rent. 
In the listings files there are included all the data about the host, the property characteristics, the amenities they include, the reviews every listing has in average.
The reviews files has millions of reviews and the clients who made them. Very nice for a NLP process. Not this time.
The calendar files has all the dates the listings are available.
The big missing value this time is the occupancy, who could had given us a lot of interesting information. We missed it.
Nevertheless we did find good data and interesting questions to work for.

## Gathering and wrangling the data - _Data Preparation_

After check the data available, and thinking about some numerical and categorical information that can be helpful for a future host of airbnb, the next questions came out:

1. **Which** is the most popular property type in Airbnb?
2. **Where** is the perfect location?
3. **What** could be my asking price?
4. **When** is better to be available?, and how the price change?
5. **Will** my property be rented?
6. **With** which features do I have to take extra care? - With machine learning approach.

All these questions were answered and some graphs and their analysis are shown in the notebook mentioned before.
Please be my guest and find out all the wrangling and programming process. 

	
## Graphs and graphs - _Results_

Please check the notebook for the graphs, results and their analysis.

You can check the resulting graphs in the next files present in this GitHub:

* q1_image_airbnb.png
* q2_image_airbnb.png
* q3_image_airbnb.png
* q4_image_airbnb.png
* q5_image_airbnb.png
* q6_image_airbnb.png


## Delivering results and thoughts - _Deployment_

Finally, after all this process, you can find my thoughts for this exercise in my blog:

[An airbnb host wannabe in London?](https://carloslarocha.medium.com/an-airbnb-host-wannabe-in-london-6088c15426a7)

Enjoy!

![alt text](airbnb_properties_london2020.png "ending")





