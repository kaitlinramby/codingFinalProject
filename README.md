# codingFinalProject
*Initial idea:*

* I had known about Hofstede’s cultural dimensions theory and thought it would be interesting to see if I could put one of these dimensions to the test and compare it to another metric. Since gender pay gaps are a big topic at the moment, I thought comparing the masculinity index to gender pay gap data on various developed countries would make for an interesting story and analysis.

*Crawling, cleaning and merging the data: BACK END*

* I found a website listing all of the values for masculinity levels from Hofstede’s research here: [http://www.clearlycultural.com/geert-hofstede-cultural-dimensions/masculinity/](http://www.clearlycultural.com/geert-hofstede-cultural-dimensions/masculinity/) 

* I took gender pay gap data from The Organisation for Economic Co-operation and Development (OECD), which is available on Wikipedia, from here: [https://en.wikipedia.org/wiki/Gender_pay_gap](https://en.wikipedia.org/wiki/Gender_pay_gap) 

* I decided to scrape the data from these pages using Python via a Jupyter notebook.

* I launched a one-click server data analysis in Digital Ocean with Python and a Jupyter Notebook installed.

* After a lot of research and reading, I used a [Medium tutorial](https://medium.com/@ageitgey/quick-tip-the-easiest-way-to-grab-data-out-of-a-web-page-in-python-7153cecfca58) combined with the information from the lessons this term in Python, to scrape the tables on the above mentioned web pages and merge them together, which you can [see in full here](https://github.com/kaitlinramby/codingFinalProject/blob/master/Hofstede%2BCultural%2BDimensions%2BProject.ipynb).

* For the Hofstede data, I crawled the table I needed from the page to get ONLY the data I needed and selected the correct header and saved it as [hofstede.csv](https://github.com/kaitlinramby/codingFinalProject/blob/master/hofstede.csv).

* I repeated this process for the gender gap data which I saved as [gender_gap_wage.csv](https://github.com/kaitlinramby/codingFinalProject/blob/master/gender_gap_wage.csv).

* As a third step in the Notebook, I used the Pandas library to merge both datasets with ‘Country’ as the common datapoint

* The result of merging the datasets is shown in the [data.csv](https://github.com/kaitlinramby/codingFinalProject/blob/master/data.csv).

* I placed this data in a google spreadsheet which was used as a datatable for my front end. After the scraping, a few countries had to be added manually as the Hofstede table I scraped was missing a few countries (some datasets online include more countries but only one dimension) so I had to browse the specific missing countries online to find the masculinity information.

* [https://docs.google.com/spreadsheets/d/12XCvZjENQebwbTmSdREmR_JwR0cj8oBu1ViWbMNuUwQ/edit?usp=sharing](https://docs.google.com/spreadsheets/d/12XCvZjENQebwbTmSdREmR_JwR0cj8oBu1ViWbMNuUwQ/edit?usp=sharing) 

I wasn’t sure what I was going to get from comparing this data, but I was actually surprised to see that many of the countries with the highest levels of masculinity either have average or very low gender pay gaps, while there were many developed countries with low masculinity levels compared to higher gender pay gap percentages (like Finland).

Instead of only doing some charts in Python in the notebook, and analysis, I wanted to try my hand at further developing my coding skills, so I also created a website for the project. Below is how I developed the front end and visualised the data.

I used the front end dev as an EDA (exploratory data analysis) step to see how the two metrics compared to one another, and if any patterns emerged.

*Analysing, visualising and sharing the results: FRONT END*

* I built the website from scratch using the Bootstrap 4 library since (a) a lot of features are already built-in with it, and (b) I wanted to learn to work with a widely used front-end tool. I was able to accomplish this by learning from several tutorials in W3Schools.

* For the week 3 assessment, I used Google Charts visualization library. Even if this is used slightly less than D3.js, I found the learning curve to be "easy" because it integrates well with Google sheets where I kept my data and all the files in my Google Drive and Google Maps for the geocharts. So, I decided to use it also for this final project.

* The hardest part of this whole project was getting the column chart to work with (binding it) the select function (dropdown).

* It took many, many hours and going through a lot of [Google Charts tutorials](https://developers.google.com/chart/interactive/docs/) to properly bind the dropdown function to the Google charts. THEN I also had to try and get the double axis to display the two metrics evenly for the column chart which resulted in a lot of fails before I was able to finally get it after playing a lot with the options and reading forums in Stackoverflow.

* I used the column chart so users can see the "big picture" pattern between the two metrics, and then they can use the selector tool to look at specific countries and compare them side by side. I then added in the geocharts to give another element to the data so users could interpret the data from another dimension.

* I hosted the website as a github page, of which you can see the final result here: [https://kaitlinramby.github.io/codingFinalProject/](https://kaitlinramby.github.io/codingFinalProject/) 

Overall, I think the visualisations are clean and professional as a result of having used the Google Charts, and the Bootstrap for the page design. I would have liked to take it a few steps further and used other cultural dimensions from Hofstede, such as individuality, and compare that to divorce rates in different countries, but I was only able to get enough work done for one comparison. Also, with more time and experience, my code could me made much shorter and cleaner.

