# Pyspark_Assignment

# Question 1
### 1.Create DataFrame as purchase_data_df,  product_data_df with custom schema with the below data 
Dataset: Column names["customer", "product_model"] : 

(1, "iphone13"), 
(1, "dell i5 core"), 
(2, "iphone13"), 
 (2, "dell i5 core"), 
 (3, "iphone13"), 
 (3, "dell i5 core"), 
 (1, "dell i3 core"), 
 (1, "hp i5 core"), 
 (1, "iphone14"), 
 (3, "iphone14"), 
 (4, "iphone13") 

Dataset: Column Names: ["product_model"] 
("iphone13",), 
("dell i5 core"), 
 ("dell i3 core"), 
 ("hp i5 core"), 
 ("iphone14") 

 <img width="1652" height="343" alt="image" src="https://github.com/user-attachments/assets/762ce4f9-9ca3-44d1-9a78-fe3ba936b52d" />
 Output
 <img width="1627" height="456" alt="image" src="https://github.com/user-attachments/assets/b4cc5c5f-40e4-417f-9c0c-283bbb26db96" />

### 2.Find the customers who have bought only iphone13 

<img width="1640" height="372" alt="image" src="https://github.com/user-attachments/assets/eb16f988-fd55-4dd2-9e60-ff897cc10212" />

Output
<img width="1617" height="123" alt="image" src="https://github.com/user-attachments/assets/090105e6-499b-43f6-9f71-9a09fc327e89" />

### 3.Find customers who upgraded from product iphone13 to product iphone14 
<img width="1657" height="417" alt="image" src="https://github.com/user-attachments/assets/797ba93e-0eae-43ca-800a-4eb2dd2a443c" />
Output
<img width="1490" height="182" alt="image" src="https://github.com/user-attachments/assets/90cf8759-cf1e-467d-af63-e6d9b53a176e" />

### 4.Find customers who have bought all models in the new Product Data 
<img width="1868" height="456" alt="image" src="https://github.com/user-attachments/assets/4992972d-c6df-45d0-99ad-759108519708" />
output
<img width="1717" height="117" alt="image" src="https://github.com/user-attachments/assets/cd49bc29-cdd8-4c89-a503-961a62556f84" />

# Question 2
DataSet:Column(“card_number”) ("1234567891234567",), ("5678912345671234",), ("9123456712345678",), ("1234567812341122",), ("1234567812341342",)
### 1.Create a Dataframe as credit_card_df with different read methods
<img width="1867" height="317" alt="image" src="https://github.com/user-attachments/assets/9c99c2a0-16bd-4753-8b43-0ccec628f668" />

B) Using spark.read.csv()
<img width="1657" height="57" alt="image" src="https://github.com/user-attachments/assets/8ddf6886-9946-4597-b6b3-67c84b85f7d6" />

C) Using spark.read.text()
<img width="1636" height="52" alt="image" src="https://github.com/user-attachments/assets/0b944e9d-1f9b-49d0-90bb-677ad2c1ca1c" />

### 2. Print number of partitions
<img width="1051" height="60" alt="image" src="https://github.com/user-attachments/assets/2ea3f88c-d02a-4355-b4cf-3127b34af92a" />
output
<img width="1155" height="37" alt="image" src="https://github.com/user-attachments/assets/77b7560f-b273-47a0-a734-aada0f2b2019" />

### 3. Increase partition size to 5
<img width="1230" height="71" alt="image" src="https://github.com/user-attachments/assets/cebd9c7a-01cd-4e49-9ba1-46c9f880291e" />
output
<img width="1112" height="30" alt="image" src="https://github.com/user-attachments/assets/fc29ead1-aa96-4f7a-afec-5ae54500805b" />

### 4. Decrease partition size back to original
<img width="1586" height="80" alt="image" src="https://github.com/user-attachments/assets/8b29ccd9-1d9b-42da-9159-c25acccb4e21" />

output
<img width="1573" height="42" alt="image" src="https://github.com/user-attachments/assets/559cd0c7-5e2b-41c8-88cc-fab0274088da" />

### 5. Create UDF to mask card numbers except last 4 digits & 6. Output should have 2 columns: card_number, masked_card_number
<img width="1820" height="502" alt="image" src="https://github.com/user-attachments/assets/af15a261-24a1-4f06-96c4-b536546b08b4" />
output
<img width="1786" height="177" alt="image" src="https://github.com/user-attachments/assets/fab61d72-be67-4971-ae63-6892828444ea" />


# Question 3
### 1. Create a DataFrame with StructType + StructField
<img width="1867" height="497" alt="image" src="https://github.com/user-attachments/assets/a3cb5c5b-7751-4748-aaa5-053309ffc7e2" />

output
<img width="1623" height="222" alt="image" src="https://github.com/user-attachments/assets/963725eb-6b02-43f0-ae5a-a70d67bf7e84" />

### 2. Rename columns dynamically
<img width="1502" height="248" alt="image" src="https://github.com/user-attachments/assets/e6a8fb31-de81-4d71-98df-1173bd90e35a" />

output
<img width="1458" height="213" alt="image" src="https://github.com/user-attachments/assets/b232f211-7566-4904-966d-67eb36918ea8" />

### 3. Write a query to calculate the number of actions performed by each user in the last 7 days
<img width="1872" height="353" alt="image" src="https://github.com/user-attachments/assets/123e49b7-2480-41a9-9816-75b7e656c024" />

output
<img width="1085" height="133" alt="image" src="https://github.com/user-attachments/assets/08d6cf27-3496-4435-954a-efdf37f917c6" />

### 4. Convert time_stamp → login_date (YYYY-MM-DD, DateType)
<img width="1698" height="232" alt="image" src="https://github.com/user-attachments/assets/a4579518-7794-4a3a-8ba2-8fd7769d850f" />

output
<img width="1217" height="222" alt="image" src="https://github.com/user-attachments/assets/633fd9fd-6e3e-433c-956d-408e3df75364" />



# 4. Question

Json file Download Link: [nested_json_file.json](https://github.com/user-attachments/files/23673018/nested_json_file.json)

### 1. Read JSON file provided in the attachment using the dynamic function
<img width="1386" height="211" alt="image" src="https://github.com/user-attachments/assets/d7d40ba0-ca78-4d83-b0b0-d285ede2c0e7" />
output
<img width="1196" height="285" alt="image" src="https://github.com/user-attachments/assets/333b85e2-a839-4049-bf1b-0d21746dd543" />

### 2. Flatten the custom-schema JSON
<img width="1152" height="288" alt="image" src="https://github.com/user-attachments/assets/f4561ffa-8e7d-406e-bbd5-6667217ed672" />
output
<img width="1310" height="137" alt="image" src="https://github.com/user-attachments/assets/19b9c88c-c947-4769-9bb2-1ec2e4967d71" />

### 3. find out the record count when flattened and when it's not flattened(find out the difference why you are getting more count)
<img width="1283" height="420" alt="image" src="https://github.com/user-attachments/assets/51ae1230-3901-4b9e-8124-548d7df3b7b3" />

output
<img width="1043" height="170" alt="image" src="https://github.com/user-attachments/assets/379cd557-7935-409b-af7f-dcd4ac3cf908" />



### 4. Differentiate the difference using explode, explode outer, posexplode functions 

#### explode
<img width="1060" height="70" alt="image" src="https://github.com/user-attachments/assets/61ce4292-8b15-4bb8-811b-a034a417f0e0" />

output
<img width="995" height="148" alt="image" src="https://github.com/user-attachments/assets/24c348d8-4f85-4bcc-9e95-34c5789551cb" />

##### explode outer
<img width="1340" height="70" alt="image" src="https://github.com/user-attachments/assets/36bec68b-52a0-403d-a101-92997d2dab36" />

output
<img width="1031" height="157" alt="image" src="https://github.com/user-attachments/assets/4ebc1ccf-b28c-4843-8cb4-420907e084c6" />

##### posexplode functions
<img width="1215" height="68" alt="image" src="https://github.com/user-attachments/assets/c756875d-919f-468f-be11-7f958e689ef2" />

output
<img width="1157" height="153" alt="image" src="https://github.com/user-attachments/assets/52177677-d9a2-47db-992e-70bbf02e6bcc" />

### 5. Filter the id which is equal to 0001  
<img width="1035" height="43" alt="image" src="https://github.com/user-attachments/assets/59497696-fdc5-41fb-a1fb-fd5a279b0b82" />

Output
<img width="937" height="63" alt="image" src="https://github.com/user-attachments/assets/1e473606-9578-44f3-9241-3d0f8d946489" />

### 6. convert the column names from camel case to snake case 
<img width="1467" height="151" alt="image" src="https://github.com/user-attachments/assets/6dc45982-c6df-4753-8552-a849f1106f01" />

### 7. Add a new column named load_date with the current date
<img width="972" height="42" alt="image" src="https://github.com/user-attachments/assets/108a488f-6718-401e-a372-e9f502c842f0" />

Output
<img width="1182" height="138" alt="image" src="https://github.com/user-attachments/assets/828682de-b66b-4330-b88f-b14b5f8ff226" />

### 8. create 3 new columns as year, month, and day from the load_date column 
<img width="1247" height="96" alt="image" src="https://github.com/user-attachments/assets/d5135c24-a635-4b00-bb6b-4d1a097e7d0f" />

Output
<img width="1060" height="142" alt="image" src="https://github.com/user-attachments/assets/7d47eb13-9cff-40d5-a6d1-1047585a5eb9" />



# 5. Question 
DataSet1:Column names(employee id, employee_name, department, State, salary, Age) 
((11,“james”,” D101”,”ny”,9000,34)), 
(12,”michel”,” D101”,”ny”,8900,32), 
(13,“robert”,” D102”,”ca”,7900,29), 
(14,“scott”,” D103”,”ca”,8000,36), 
(15,“jen”,” D102”,”ny”,9500,38), 
(16,”jeff”,” D103”,”uk”,9100,35), 
(17,“maria”,” D101”,”ny”,7900,40)) 

Dataset2:Column names(dept_id, dept_name) 
((“D101”,”sales”), 
(“D102”,”finance”), 
(”D103”,”marketing”), 
(“D104”,”hr”), 
(“D105”,”support”)) 
 
Dataset3: Column names(country_code, country_name) 
((“ny”,”newyork”), 
(“ca”,”California”), 
(“uk”,”Russia)) 

### 1. create all 3 data frames as employee_df, department_df, country_df with custom schema defined in dynamic way 
<img width="1433" height="925" alt="image" src="https://github.com/user-attachments/assets/39ec9a9f-af23-49d0-8782-9750c0597021" />

### 2. Find avg salary of each department 
<img width="1330" height="97" alt="image" src="https://github.com/user-attachments/assets/3f36193a-23da-4054-9b90-917fe81b41e7" />

Output
<img width="1073" height="135" alt="image" src="https://github.com/user-attachments/assets/4d4661f5-4350-49e0-a6e4-ae0ce426643f" />

### 3. Find the employee’s name and department name whose name starts with ‘m’  
<img width="1560" height="83" alt="image" src="https://github.com/user-attachments/assets/013d3f93-ee00-4272-897e-b49d8924debe" />

Output
<img width="997" height="107" alt="image" src="https://github.com/user-attachments/assets/9d289658-ba32-4dff-af50-e8f5974ef06a" />

### 4. Create another new column in  employee_df as a bonus by multiplying employee salary *2 
<img width="1073" height="38" alt="image" src="https://github.com/user-attachments/assets/1b0366c4-3808-48c4-b8a5-42e72db11a61" />

Output
<img width="1087" height="206" alt="image" src="https://github.com/user-attachments/assets/7fed9050-651f-4712-8844-9ccf922e3ea5" />

### 5. Reorder the column names of employee_df columns as (employee_id,employee_name,salary,State,Age,department,bonus) 
<img width="1323" height="37" alt="image" src="https://github.com/user-attachments/assets/9f7cb28c-b27b-4e34-96a8-7e102110210d" />

Output
<img width="1317" height="206" alt="image" src="https://github.com/user-attachments/assets/a621e4b4-0763-4cc7-986d-21b7a4460949" />

### 6. Give the result of an inner join, left join, and right join when joining employee_df with department_df in a dynamic way 

inner join
<img width="1367" height="122" alt="image" src="https://github.com/user-attachments/assets/3ab3a5a8-c372-4b9a-910a-5b1a8ff87d08" />

Output
<img width="1502" height="218" alt="image" src="https://github.com/user-attachments/assets/be428178-9d41-48ac-9927-561d1bb7ee2d" />

left join
<img width="1182" height="77" alt="image" src="https://github.com/user-attachments/assets/2a9ccab7-6f0b-4086-8067-f71af3b8ef03" />

Output
<img width="1416" height="227" alt="image" src="https://github.com/user-attachments/assets/869f9955-9345-485f-b2e4-474b5e89ef0e" />

right join
<img width="1155" height="67" alt="image" src="https://github.com/user-attachments/assets/645d88f9-71ec-4b7a-8941-4101097cb289" />

Output
<img width="1323" height="262" alt="image" src="https://github.com/user-attachments/assets/cb53eb89-c15e-4559-bbf2-5a328c10202c" />

### 7. Derive a new data frame with country_name instead of State in employee_df  
##### Eg(11,“james”,”D101”,”newyork”,8900,32) 
<img width="1150" height="202" alt="image" src="https://github.com/user-attachments/assets/374be50c-29f8-4878-8756-f5ee0ce13ae8" />

Output
<img width="1321" height="198" alt="image" src="https://github.com/user-attachments/assets/7063630c-a1c7-4954-9d0e-ee2f0e2c00b3" />

### 8. convert all the column names into lowercase from the result of question 7in a dynamic way, add the load_date column with the current date 
<img width="1332" height="233" alt="image" src="https://github.com/user-attachments/assets/919afeac-c25e-40e6-91dc-f03f85d024d4" />

Output
<img width="1323" height="222" alt="image" src="https://github.com/user-attachments/assets/8c887079-a764-4a74-9fd3-8adbee4a5d6c" />


















