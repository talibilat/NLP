##Stock Sentiment Analysis using News Headlines
This project uses news headlines from the year 2000 to 2014 to perform sentiment analysis on stock prices. The dataset used for this project is in the form of a CSV file and contains 25 top news headlines for each day. The goal of this project is to use these headlines to predict whether the stock market will go up or down.

Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

Prerequisites
Python 3
Pandas library
Installing
Clone the repository to your local machine
Copy code
git clone https://github.com/[username]/Stock-Sentiment-Analysis-using-News-Headlines.git
Install the required libraries by running the following command in the terminal
Copy code
pip install -r requirements.txt
Running the code
Run the following command in the terminal to execute the code
Copy code
python Sentiment.py
Code Explanation
The code starts by importing the necessary libraries, in this case, we are using pandas to read the CSV file.

Copy code
import pandas as pd
The CSV file is then read and the first five rows are displayed to give an idea of the dataset.

Copy code
df=pd.read_csv('Data.csv', encoding = "ISO-8859-1")
df.head()
The dataset is then split into training and testing sets with the training set containing data until the year 2014 and the testing set containing data from 2015.

Copy code
train = df[df['Date'] < '20150101']
test = df[df['Date'] > '20141231']
The code then removes any punctuations from the dataset and renames the columns for ease of access.

Copy code
data=train.iloc[:,2:27]
data.replace("[^a-zA-Z]"," ",regex=True, inplace=True)
list1= [i for i in range(25)]
new_Index=[str(i) for i in list1]
data.columns= new_Index
The code then proceeds to perform the sentiment analysis on the dataset using Natural Language Processing techniques.

Authors
[Your Name] - Initial work - Your github link
License
This project is licensed under the MIT License - see the LICENSE.md file for details

Acknowledgments
Hat tip to anyone whose code was used
Inspiration
etc
