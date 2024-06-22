# Austin Animal Center Outcomes #

This data set was collected from [Data.gov](Data.gov) 

At time of downloading the csv file, the data set spans  
from 01/01/2014 thru 12/31/2023.  

**Intro to the data from Data.gov**

-Outcomes represent the status of animals as they leave the Animal Center.  
-All animals receive a unique Animal ID during intake.  
-Annually over 90% of animals entering the center, are adopted, transferred to rescue  
or returned to their owners.  
-The Outcomes data set reflects that Austin, TX. is the largest "No Kill" city in the country.

If you would like to know more about Austin Animal Center  
you can visit their site here-  
[Austin Animal Center](https://www.austintexas.gov/austin-animal-center)  

This is my first uploaded notebook using python to analyze data.  
I first imported **pandas** and **matplotlib.pyplot** for reading the csv file  
and to create a few visual graphs for representation of the data. 

I wanted to explore this data with more attention to the outcome type "**Euthanasia**".  
There are a few different Animal Types this data holds and was interesting   
learning about all the data collected in this data set. 


 ### First Things First ###

**Review and clean the data.**  
I named the data frame austin_df  
Looking through the data I noticed a few duplicates so I wanted to drop those. 
```python
austin_df.drop_duplicates()
```

**24** rows dropped from the set. For a total of **162,827** rows of data.  

There were columns within this data that I would not be using and a date/time that  
I only needed the MM/DD/YYYY. I left the columns in tack but decided to split the time from the date.  
```python
austin_df['Date In'] = austin_df['DateTime'].apply(lambda x: x[0:10])
```

### Questions ###
1. What are the different outcome types?
2. How are they labeled?
3. What are the different Animal Types?
4. What are the different Outcome Sub-types for Euthanized animals?


There were **11** different outcome types.    
#### Top 4 Outcome Types- ####
1. **Adoption**- 77,631 records
2. **Transfer**- 46,438 records
3. **Return to Owner**- 24,906
4. **Euthanasia**- 24,906


There were **5** different animal types.
1. **Dog**- 89,748 records
2. **Cat**- 63,778 records
3. **Other**- 8,485 records
4. **Bird**- 815 records
5. **Livestock**- 2 records

With this information I began to breakdown each of the different animal types.  
I wrote code to pull information about each and provide a visual representation  
using matplotlib.pyplot.

This was a very fun project that has much more in depth information  
within and I am excited to explore the other outcomes and provide insites to what  
it will tell. 

#### **Contributing** ####
Contributions are welcome!  
Please open an issue or submit a pull request for any improvements or additions.

#### **License** ####
This project is licensed under the MIT License - see the LICENSE file for details.

#### **Acknowledgments** ####
Publisher- **data.austintexas.gov** for providing the dataset.  
The data science community for continuous support and resources.