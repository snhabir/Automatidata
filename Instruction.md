In this lab portion of the end-of-course project, you will open a Jupyter Notebook and follow instructions to enter code and written responses were prompted.

# **Data dictionary**

This project uses a dataset called **2017\_Yellow\_Taxi\_Trip\_Data.csv**. It is data gathered by the New York City Taxi & Limousine Commission and published by the city of New York as part of their NYC Open Data program. In order to improve the learning experience and shorten runtimes, a sample was drawn from the 113 million rows in the 2017 Yellow Taxi Trip Data table.

The dataset contains:

22,699 rows – each row represents a different trip

18 columns

| Column name | Description |
| :---- | :---- |
| ID | Trip identification number |
| VendorID | A code indicating the TPEP provider that provided the record.  1= Creative Mobile Technologies, LLC; 2= VeriFone Inc. |
| tpep\_pickup\_datetime  | The date and time when the meter was engaged.  |
| tpep\_dropoff\_datetime  | The date and time when the meter was disengaged.  |
| Passenger\_count  | The number of passengers in the vehicle.   This is a driver-entered value. |
| Trip\_distance  | The elapsed trip distance in miles reported by the taximeter. |
| PULocationID  | TLC Taxi Zone in which the taximeter was engaged |
| DOLocationID  | TLC Taxi Zone in which the taximeter was disengaged |
| RateCodeID  | The final rate code in effect at the end of the trip.  1= Standard rate  2=JFK  3=Newark  4=Nassau or Westchester  5=Negotiated fare  6=Group ride |
| Store\_and\_fwd\_flag  | This flag indicates whether the trip record was held in vehicle memory before being sent to the vendor, aka “store and forward,”  because the vehicle did not have a connection to the server.  Y= store and forward trip  N= not a store and forward trip |
| Payment\_type  | A numeric code signifying how the passenger paid for the trip.  1= Credit card  2= Cash  3= No charge  4= Dispute  5= Unknown  6= Voided trip |
| Fare\_amount  | The time-and-distance fare calculated by the meter. |
| Extra  | Miscellaneous extras and surcharges. Currently, this only includes the $0.50 and $1 rush hour and overnight charges. |
| MTA\_tax  | $0.50 MTA tax that is automatically triggered based on the metered rate in use. |
| Improvement\_surcharge  | $0.30 improvement surcharge assessed trips at the flag drop. The  improvement surcharge began being levied in 2015\. |
| Tip\_amount  | Tip amount – This field is automatically populated for credit card tips. Cash tips are not included. |
| Tolls\_amount  | Total amount of all tolls paid in trip.  |
| Total\_amount  | The total amount charged to passengers. Does not include cash tips. |

Remember, you can access and download the data for any Jupyter notebook activity from within the notebook itself by navigating to the **Lab Files** dropdown menu at the top of the page, clicking into the **/home/jovyan/work** folder,  selecting the relevant data file, and clicking **Download**.

Refer to [NYC Open Data](https://data.cityofnewyork.us/Transportation/2017-Yellow-Taxi-Trip-Data/biws-g3hs) for more information related to this dataset.

# **Access the end-of-course project lab**

*Note: Click the Open Lab button to start your end-of-course project lab. Once you complete this activity, click Next to continue on to the exemplar reading.*

(Lab) Activity Instructions: 

The Jupyter Notebook will autosave as you work, or you can manually save it by clicking the Save and Checkpoint button or by selecting Save and Checkpoint from the File menu.   
![][image1]

As you complete the end-of-course project lab, note the following features:

* Sections: Step-by-step instructions in each section lead you through the lab.  
* Code blocks: Code blocks allow you to practice key Python coding concepts. Add code where prompted and then click the Run button to execute your code and view any possible output.

![][image2]

* Questions: Thought questions offer moments to pause and think about concepts and your output as you move through the lab.

To review how to work in Jupyter Notebooks, refer to the reading [Practice Python skills in Jupyter Notebooks](https://www.coursera.org/teach/google-beginning-your-python-journey/authoringBranch~wJKPci8PEe-YcA77IVc2yQ/content/item/supplement/C2ll0).

Be sure to complete this lab before moving on. The next course item will explain how to review an exemplar of a completed end-of-course project lab. You can compare the code and text responses in the exemplar to your own.  


[image1]: <data:image/png;base64,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>

[image2]: <data:image/png;base64,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>