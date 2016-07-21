# Salesforce Processing with Batch Apex

* Salesforce Batch processing that allows bypassing of Salesforce governor limits (50,000 records received from SOQL query and 10,000 DML operations)
* Used Visualforce, Apex, Batch Apex
* This functionality was added to original processing to allow the client to process more than 10,000 records at once

Demo:
---

###Query & Process Selected

<img src="https://raw.github.com/elizabethtian/salesforce-batch-processing/master/img/query.png"/>

* Process cards component allows the organization to filter by card company, card type, month, and year
* When "Query" button is clicked, all "Income" records matching the filter criteria are displayed, if the number of records is under 1000
* Records can be selected and processed through the "Process Selected" button

###Process All

<img src="https://raw.github.com/elizabethtian/salesforce-batch-processing/master/img/processall.png"/>

* If number of records is over 1000 they are not displayed
* Clicking the "Process All" button will process all the records that match the displayed filter criteria, even if there are over 10,000 records

###Check Status

<img src="https://raw.github.com/elizabethtian/salesforce-batch-processing/master/img/check.png"/>

####Status Messages

<img src="https://raw.github.com/elizabethtian/salesforce-batch-processing/master/img/processing.jpg"/>

<img src="https://raw.github.com/elizabethtian/salesforce-batch-processing/master/img/completed.png"/>

* The "Check 'Process All' Status" button can be used to check the status of the Apex batches that were sent for processing
* Each Apex batch is 200 records, processed asynchronously to bypass governor limits 
