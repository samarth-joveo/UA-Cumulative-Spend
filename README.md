# UA-Cumulative-Spend
![image](https://user-images.githubusercontent.com/104884127/224625987-37d00cf4-0563-4ac1-bfbf-6c14ec6ba63e.png)
Assumption: Order of columns selected in looker - Date, Daily Spend, Cumulative Spend. 
</br>Data Selected in Looker : 
Date is a dimenion, Spend is a measure and Cumulative Spend is a table calculation.
Cumulative Spend formula : running_total(${view_grouped_tracking_event.cdspend})
![image](https://user-images.githubusercontent.com/104884127/224626501-fee83e1c-141b-4eba-8d4e-532df1ca8c58.png)
Format of the data flowing to looker custom visual :
</br>data = [</br>
{ 'Date':{ 'value' : '2023-01-01' } , 'spend' : { 'value' : 100 } , 'cumulative_spend' : { 'value' : 100 }, 'max_date' : { 'value' : '2023-01-15' } },</br>
{ 'Date':{ 'value' : '2023-01-02' } , 'spend' : { 'value' : 100 } , 'cumulative_spend' : { 'value' : 200 }, 'max_date' : { 'value' : '2023-01-15' } },</br>
{ 'Date':{ 'value' : '2023-01-03' } , 'spend' : { 'value' : 100 } , 'cumulative_spend' : { 'value' : 300 }, 'max_date' : { 'value' : '2023-01-15' } },</br>
{ 'Date':{ 'value' : '2023-01-04' } , 'spend' : { 'value' : 100 } , 'cumulative_spend' : { 'value' : 400 }, 'max_date' : { 'value' : '2023-01-15' } }</br>
]</br>
