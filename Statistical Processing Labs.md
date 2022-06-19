Disclaimer: All Rights Reserved. All the material is self created and not copied from somewhere. This is a solution guide to Splunk Training Labs present on education.splunk. I give anyone rights to use the material in a form to help increase your knowledge.

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
Suggesation: split events by 1st field i.e vendor_action. Then the count for failed and accepted will be shown. Then the multivalue split comes into picture and add by src_ip. The Chart virtualizaition will be further split by src_ips.
 
![image](https://github.com/ShahzebFarruk/Splunk_Material/blob/main/Statistical%20Labs/table3.png)

Save your search as a report with the name L1S2. 
 
## Task 4: Complete a search with the chart command to create a multi-series visualization. 
Scenario: Sales wants to know the 5 best-selling products for North American vendors over the previous week. 

Complete the <missing> portion of this search with the chart command so that the output displays a count of events for each VendorCountry. Run the search over the Previous week. (Note: The basic search contains VendorID<4000 because in our environment the VendorIDs for North American countries are 1000 – 2999 for USA and 3000 – 3999 for Canada.) 

index=sales sourcetype=vendor_sales VendorID<4000 | <missing> 
Split your data by product_name to see a count of each product sold in USA and Canada. 
Finally, edit the chart command so that only the top 5 best-selling products are displayed without an OTHER category. 



```spl
index=sales sourcetype=vendor_sales VendorID<4000 
| chart count over VendorCountry by product_name useother=f limit=5
```
Save your search as a report with the name L1S 3 .
![image](https://github.com/ShahzebFarruk/Splunk_Material/blob/main/Statistical%20Labs/table4.png)

##  Task 5: Use the top command to identify which domains website visitors are using
Scenario: Sales and Marketing want to know the two most popular referrer domains our website users are coming from.


