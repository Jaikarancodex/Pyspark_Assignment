[nested_json_file.json](https://github.com/user-attachments/files/23673018/nested_json_file.json)# Pyspark_Assignment

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































