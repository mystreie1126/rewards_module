
<h1>1. Roll Back Entry</h1> 

<h2>From the Funtechglobaldatabase:</h2>

<img src="https://github.com/JianNCI/rewards_module/blob/master/reward_screenshot/issue_status.png"> 

<p> :speaker: From the track-><b>issue_status</b> table we found there are all the status with its ID, 
so we can know which ID  is represents which issue status, such as ID<b>4</b> represents <b><i>payment accepted and closed</i></b>

<img src="https://github.com/JianNCI/rewards_module/blob/master/reward_screenshot/issue_history.png">
<p> :speaker: Above image shows the every issue_history record associate with issse_status ID individually</p>


<p>:runner: if a staff closed the entry by mistake, just look for the <b>issue_status</b> table with the given issue number such as FTM00000MC
Find the row with status_id = 4 and change the status_id to any other number, which means this repair entry is not payment recieved 
and closed</p> 

<p>Change the status id of a repair, remember the id of this repair/entry and find the entry id from the issue_history table. Delete all the rows which has 
status id equals to 4,which means re-open the entry</p> 



<h1>2. Removed the parts usage on a single repair/entry <h1>
  
<p>:runner:Given issue code: <b><i>FT02261018PY</i></b> with Sohail add the wrong parts to the repair,needs to removed from that repiar and adds the correct one</p>


<p>First we should spot the <b>parts_usage</b> table with staff_id = 115(which the staff_id can be found in <b>staff</b> table)<p>
<p>Then find the rows with column value: <b><i>tracking</i></b> = '<b><i>FT02261018PY</i></b>'

<img src="https://github.com/JianNCI/rewards_module/blob/master/reward_screenshot/parts_usage.png"/>

<p>:speaker: Please note: We can simply delete that rows which means removed the parts usage from that repair, but this will leave 1 number under the pending column from the dashboard. So we need to went to <b>stock</b> table to find the stock id with issue <b><i>FT02261018PY</i></b> before we delete that row from the <b>parts_usage</b> table
