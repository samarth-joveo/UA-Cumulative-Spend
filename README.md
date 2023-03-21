# UA-Cumulative-Spend
![image](https://user-images.githubusercontent.com/104884127/224625987-37d00cf4-0563-4ac1-bfbf-6c14ec6ba63e.png)
Assumption: Order of columns selected in looker - Date, Max Date, Daily Spend, Cumulative Spend. 
<br>Projection Spend = (MTD Spend) * (Number of days in the month) / (Number of Days completed in current month)
</br>Data Selected in Looker : 
Date is a dimenion, Spend is a measure and Cumulative Spend is a table calculation.
Cumulative Spend formula : running_total(${view_grouped_tracking_event.cdspend})
![image](https://user-images.githubusercontent.com/104884127/224633870-87ac2497-172d-4b78-ac40-95ee74597352.png)
Format of the data flowing to looker custom visual :
</br>data = [</br>
{ 'Date':{ 'value' : '2023-01-01' } ,  'max_date' : { 'value' : '2023-01-15' } , 'spend' : { 'value' : 100 } , 'cumulative_spend' : { 'value' : 100 }, 'budget_cap' : {'value' : 20} },</br>
{ 'Date':{ 'value' : '2023-01-02' } ,  'max_date' : { 'value' : '2023-01-15' } , 'spend' : { 'value' : 100 } , 'cumulative_spend' : { 'value' : 200 }, 'budget_cap' : {'value' : 20} },</br>
{ 'Date':{ 'value' : '2023-01-03' } ,  'max_date' : { 'value' : '2023-01-15' } , 'spend' : { 'value' : 100 } , 'cumulative_spend' : { 'value' : 300 }, 'budget_cap' : {'value' : 20} },</br>
{ 'Date':{ 'value' : '2023-01-04' } ,  'max_date' : { 'value' : '2023-01-15' } , 'spend' : { 'value' : 100 } , 'cumulative_spend' : { 'value' : 400 }, 'budget_cap' : {'value' : 20} }</br>
]</br>
