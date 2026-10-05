Healthcare Data Analysis and Insights
Module End Assignment 1 – Excel
 
 
Data Cleaning:
 
1: We can find the missing data using filter option. From each column we can check whether there exist any cell containing “?”.
2: The missing data can be filled using find and replace option. It has to be done through each column separately. From find and replace we can give “?” in the place of find column and correspond data in the replace column.
3: To find most frequently occurring value we can use countif(range,criteria).
EG:=COUNTIF(G1:G2344,O2)
Most frequently occurred data in
Hospital tier: tier 2
City tier: tier 2
Hence in both cases missing value is replaced by tier 2.
4: State id missing value is considered as unknown.
 
 
Data Transformation
 
1: To split the names I had used text to column option is selected.
Select the cell à text to column à delimeted
2: it can converted using if condition
=if(G2= “No major surgeries”,0,G2) and relative reference remaining value is changed.
3:inconsistencies is changed using proper()
4: Weight status column can be created using nested if
Eg: =IF(B2>$P$9,"Obesity",IF(B2>25,"Over Weight",IF(B2>18.5,"Normal Weight","Under Weight")))
5: Diabetes column can be updated as
Eg: =IF(C2>=6.5,"Diabetes",IF(C2>=5.7,"Prediabetes","Normal"))
6: Merging can be done using concat option
=CONCAT(D2,"-",C2,"-",B2)
7: to find the age datedif option is used.
=DATEDIF(J2,$O$13,"Y")
8: Charges column can be changed to currency by
In home change general option to currency.
 
 
Data Exploration , Analysis and visualization
 
Created a new worksheet named ‘Healthcare’ to combine the required data.
* Used a common ID/unique value to match records between the sheets.
We can get common id through
='Customer Names'!A2
* Apply the VLOOKUP function to retrieve the required information from other sheets.
* Example: =VLOOKUP(A2,'Customer Names'!A:E,3,FALSE)
Using this we can get the first in the customer name sheet. Similarly we can get all required data from different sheet using vlookup.
 
 
2: Now all the datas are cleaned and made a new sheet. To create a pivot table we have to first make the existing dataset into table. Once the table is created pivot table option is available on the top left corner of the sheet.
The pivot table will be created in a new sheet. And we can drag an drop the datas as per requirements.
After creating the pivot table different types of charts option is available in the insert option.
