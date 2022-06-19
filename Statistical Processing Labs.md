## Task 1: Log into Splunk and change the account name and time zone. 

 

## Task 2: Complete a search with the timechart command to create a multi-series visualization. 
Scenario: The Network team wants to add a dashboard panel that displays internet usage over the last  24 hours.

Count usage events from the web security appliance data by completing the <missing> portion of the search with the timechart command. Run the search over the Last 24 hours. 

index=network sourcetype=cisco_wsa_squid | < missing >  
![image](https://github.com/ShahzebFarruk/Splunk_Material/blob/main/Statistical%20Labs/table1.png)


Visualize results as a Line Chart.
  

![image](https://github.com/ShahzebFarruk/Splunk_Material/blob/main/Statistical%20Labs/table2.png)

  
Save your search as a report with the name L1S1.

```spl
  index=network sourcetype=cisco_wsa_squid
| timechart count by usage
  ```


  
## Task 3: Complete a search with the chart command to create a multi-series visualization. 

Scenario: Security wants to add a dashboard panel that displays the top 10 IPs associated with "Accepted" and "Failed" events on the web server.
  
  Complete the <missing> portion of the search with the chart command so that the output displays a count of events for each vendor_action value by src_ip. Run the search over the Last 24 hours. 
  
index=security sourcetype=linux_secure vendor_action!="session opened" | <missing> 

```spl
 index=security sourcetype=linux_secure vendor_action!="session opened"
| chart count over vendor_action by src_ip
 ```
![image](https://github.com/ShahzebFarruk/Splunk_Material/blob/main/Statistical%20Labs/table3.png)


