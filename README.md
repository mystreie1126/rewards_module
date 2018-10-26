
<h1>1. Roll Back Entry</h1> 

<h2>When a staff closed an Entry by mistake :pencil2:</h2>

From the Funtechglobaldatabase: 

<img src="https://github.com/JianNCI/rewards_module/blob/master/reward_screenshot/issue_status.png"> 

<p> :speaker: From the track->issue_status table we found there are all the status with its ID, 
so we can know which ID  is represents which issue status, such as ID<b>4</b> represents <b><i>payment accepted and closed</i></b>

<img src="https://github.com/JianNCI/rewards_module/blob/master/reward_screenshot/issue_history.png">
<p> :speaker: Above image shows the every issue_history record associate with issse_status ID individually</p>


<p>:runner: if a staff closed the entry by mistake, just look for the <b>issue_status</b> table with the given issue number such as FTM00000MC
Find the row with status_id = 4 and change the status_id to any other number, which means re-open this repair entry</p> 

<p>After re-open the entry, remember the id of this entry/issue and find the issue_id into the issue_history table. Delete all the rows which has 
status id equals to 4</p> 

