# 🚀 PySpark Assignment 

---

## 🎯 Question 1

### ✔ 1. Create DataFrame as `purchase_data_df`, `product_data_df` with custom schema

**Dataset — `purchase_data_df` (customer, product_model):**

```
(1, "iphone13")
(1, "dell i5 core")
(2, "iphone13")
(2, "dell i5 core")
(3, "iphone13")
(3, "dell i5 core")
(1, "dell i3 core")
(1, "hp i5 core")
(1, "iphone14")
(3, "iphone14")
(4, "iphone13")
```

**Dataset — `product_data_df` (product_model):**

```
("iphone13")
("dell i5 core")
("dell i3 core")
("hp i5 core")
("iphone14")
```

#### Code
![purchase_output](https://github.com/user-attachments/assets/762ce4f9-9ca3-44d1-9a78-fe3ba936b52d)

#### Output
![purchase_output2](https://github.com/user-attachments/assets/b4cc5c5f-40e4-417f-9c0c-283bbb26db96)

---

### ✔ 2. Find customers who have bought only `iphone13`

**Description:** Identify customers whose purchases contain only `iphone13` (no other product_model).
#### code
![only_iphone13_input](https://github.com/user-attachments/assets/eb16f988-fd55-4dd2-9e60-ff897cc10212)

#### Output
![only_iphone13_output](https://github.com/user-attachments/assets/090105e6-499b-43f6-9f71-9a09fc327e89)

---

### ✔ 3. Find customers who upgraded from `iphone13` → `iphone14`

**Description:** Customers who at any time purchased `iphone13` and later purchased `iphone14`. If timestamps/order not available, interpret as customers who have both `iphone13` and `iphone14`.

#### Code
![upgrade_input](https://github.com/user-attachments/assets/797ba93e-0eae-43ca-800a-4eb2dd2a443c)

#### Output
![upgrade_output](https://github.com/user-attachments/assets/90cf8759-cf1e-467d-af63-e6d9b53a176e)

---

### ✔ 4. Find customers who bought ALL models in `product_data_df`

**Description:** Customers whose purchased product_model set covers every model in `product_data_df`.

#### Code
![all_models_input](https://github.com/user-attachments/assets/4992972d-c6df-45d0-99ad-759108519708)

#### Output
![all_models_output](https://github.com/user-attachments/assets/cd49bc29-cdd8-4c89-a503-961a62556f84)

---

## 🎯 Question 2 — Credit Card Masking

**Dataset — `card_number`:**
```
"1234567891234567"
"5678912345671234"
"9123456712345678"
"1234567812341122"
"1234567812341342"
```

### ✔ 1. Create `credit_card_df` (different read methods)

#### Code
**A) From python list:**
![read_methods](https://github.com/user-attachments/assets/9c99c2a0-16bd-4753-8b43-0ccec628f668)

**B) Using `spark.read.csv()`**
![read_csv](https://github.com/user-attachments/assets/8ddf6886-9946-4597-b6b3-67c84b85f7d6)

**C) Using `spark.read.text()`**
![read_text](https://github.com/user-attachments/assets/0b944e9d-1f9b-49d0-90bb-677ad2c1ca1c)

---

### ✔ 2. Print number of partitions

#### Code
![partitions_cmd](https://github.com/user-attachments/assets/2ea3f88c-d02a-4355-b4cf-3127b34af92a)

#### Output
![partitions_out](https://github.com/user-attachments/assets/77b7560f-b273-47a0-a734-aada0f2b2019)

---

### ✔ 3. Increase partitions to 5

#### Code
![repartition5](https://github.com/user-attachments/assets/cebd9c7a-01cd-4e49-9ba1-46c9f880291e)

#### Output
![repartition5_out](https://github.com/user-attachments/assets/fc29ead1-aa96-4f7a-afec-5ae54500805b)

---

### ✔ 4. Decrease partitions back to original

#### Code
![repartition_orig](https://github.com/user-attachments/assets/8b29ccd9-1d9b-42da-9159-c25acccb4e21)

#### Output
![repartition_orig_out](https://github.com/user-attachments/assets/559cd0c7-5e2b-41c8-88cc-fab0274088da)

---

### ✔ 5. Create UDF to mask card numbers except last 4 digits

#### Code
![mask_udf](https://github.com/user-attachments/assets/af15a261-24a1-4f06-96c4-b536546b08b4)

#### Output
![mask_output](https://github.com/user-attachments/assets/fab61d72-be67-4971-ae63-6892828444ea)

---

## 🎯 Question 3

### ✔ 1. Create a DataFrame with `StructType` + `StructField`

**Dataset:**
```
(1, 101, 'login',  '2023-09-05 08:30:00'),
(2, 102, 'click',  '2023-09-06 12:45:00'),
(3, 101, 'click',  '2023-09-07 14:15:00'),
(4, 103, 'login',  '2023-09-08 09:00:00'),
(5, 102, 'logout', '2023-09-09 17:30:00'),
(6, 101, 'click',  '2023-09-10 11:20:00'),
(7, 103, 'click',  '2023-09-11 10:15:00'),
(8, 102, 'click',  '2023-09-12 13:10:00')
```

#### Code
![struct_schema](https://github.com/user-attachments/assets/a3cb5c5b-7751-4748-aaa5-053309ffc7e2)

#### Output
![struct_schema_out](https://github.com/user-attachments/assets/963725eb-6b02-43f0-ae5a-a70d67bf7e84)

---

### ✔ 2. Rename columns dynamically

#### Code
![rename_cols](https://github.com/user-attachments/assets/e6a8fb31-de81-4d71-98df-1173bd90e35a)

#### Output
![rename_out](https://github.com/user-attachments/assets/b232f211-7566-4904-966d-67eb36918ea8)

---

### ✔ 3. Number of actions by each user in the last 7 days

#### Code
![actions_last7](https://github.com/user-attachments/assets/123e49b7-2480-41a9-9816-75b7e656c024)

#### Output
![actions_last7_out](https://github.com/user-attachments/assets/08d6cf27-3496-4435-954a-efdf37f917c6)

---

### ✔ 4. Convert `time_stamp` → `login_date` (YYYY-MM-DD, DateType)


#### Code
![to_date](https://github.com/user-attachments/assets/a4579518-7794-4a3a-8ba2-8fd7769d850f)

#### Output
![to_date_out](https://github.com/user-attachments/assets/633fd9fd-6e3e-433c-956d-408e3df75364)

---

## 🎯 Question 4 — Nested JSON file processing

**JSON file (uploaded):** `/mnt/data/nested_json_file.json`

**(You can download / inspect that file at the above path.)**

#### Code
![json_read](https://github.com/user-attachments/assets/d7d40ba0-ca78-4d83-b0b0-d285ede2c0e7)

#### Output
![json_read_out](https://github.com/user-attachments/assets/333b85e2-a839-4049-bf1b-0d21746dd543)

---

### ✔ 2. Flatten the custom-schema JSON

#### Code
![flatten](https://github.com/user-attachments/assets/f4561ffa-8e7d-406e-bbd5-6667217ed672)

#### Output
![flatten_out](https://github.com/user-attachments/assets/19b9c88c-c947-4769-9bb2-1ec2e4967d71)

---

### ✔ 3. Record count — flattened vs not flattened (and why)

**Explanation:** The `employees` field is an array. Flattening with `explode` creates one row per array element, increasing total rows. In the uploaded file there are 3 employee elements, so flattened rows > original rows.

#### Code
![count_compare](https://github.com/user-attachments/assets/51ae1230-3901-4b9e-8124-548d7df3b7b3)

#### Output
![count_compare_out](https://github.com/user-attachments/assets/379cd557-7935-409b-af7f-dcd4ac3cf908)

---

### ✔ 4. Difference using `explode`, `explode_outer`, `posexplode`

#### Code
**explode:** drops rows when array is null, expands each element. 
![explode_cmd](https://github.com/user-attachments/assets/61ce4292-8b15-4bb8-811b-a034a417f0e0)

#### Output
![explode_out](https://github.com/user-attachments/assets/24c348d8-4f85-4bcc-9e95-34c5789551cb)

**explode_outer:** keeps rows even if array is null (fills null).  
![explode_outer_cmd](https://github.com/user-attachments/assets/36bec68b-52a0-403d-a101-92997d2dab36)

#### Output
![explode_outer_out](https://github.com/user-attachments/assets/4ebc1ccf-b28c-4843-8cb4-420907e084c6)

**posexplode:** returns (pos, element) pairs where pos is index.
![posexplode_cmd](https://github.com/user-attachments/assets/c756875d-919f-468f-be11-7f958e689ef2)

#### Output
![posexplode_out](https://github.com/user-attachments/assets/52177677-d9a2-47db-992e-70bbf02e6bcc)

---

### ✔ 5. Filter `id` equal to `"0001"`

**Note:** Uploaded JSON has `id: 1001`, not `"0001"`. Filtering `"0001"` returns zero rows.

#### Code
![filter_id_cmd](https://github.com/user-attachments/assets/59497696-fdc5-41fb-a1fb-fd5a279b0b82)

#### Output
![filter_id_out](https://github.com/user-attachments/assets/1e473606-9578-44f3-9241-3d0f8d946489)

---

### ✔ 6. Convert camelCase column names → snake_case

#### Code
![camel_to_snake](https://github.com/user-attachments/assets/6dc45982-c6df-4753-8552-a849f1106f01)

---

### ✔ 7. Add `load_date` = current date

#### Code
![load_date_cmd](https://github.com/user-attachments/assets/108a488f-6718-401e-a372-e9f502c842f0)

#### Output
![load_date_out](https://github.com/user-attachments/assets/828682de-b66b-4330-b88f-b14b5f8ff226)

---

### ✔ 8. Create `year`, `month`, `day` from `load_date`

#### Code
![ymd_cmd](https://github.com/user-attachments/assets/d5135c24-a635-4b00-bb6b-4d1a097e7d0f)

#### Output
![ymd_out](https://github.com/user-attachments/assets/7d47eb13-9cff-40d5-a6d1-1047585a5eb9)

---

## 🎯 Question 5 — Employee / Department / Country joins & transformations

### Datasets

**Dataset1 — employee_df (employee_id, employee_name, department, State, salary, Age):**
```
(11, "james", "D101", "ny", 9000, 34),
(12, "michel","D101","ny",8900,32),
(13,"robert","D102","ca",7900,29),
(14,"scott","D103","ca",8000,36),
(15,"jen","D102","ny",9500,38),
(16,"jeff","D103","uk",9100,35),
(17,"maria","D101","ny",7900,40)
```

**Dataset2 — department_df (dept_id, dept_name):**
```
("D101","sales"),
("D102","finance"),
("D103","marketing"),
("D104","hr"),
("D105","support")
```

**Dataset3 — country_df (country_code, country_name):**
```
("ny","newyork"),
("ca","California"),
("uk","Russia")
```

---

### ✔ 1. Create `employee_df`, `department_df`, `country_df` with dynamic custom schema
(Use `StructType` / `StructField` as shown in earlier examples)

#### Code
![employee_schema](https://github.com/user-attachments/assets/39ec9a9f-af23-49d0-8782-9750c0597021)

---

### ✔ 2. Average salary per department

#### Code
![avg_salary_cmd](https://github.com/user-attachments/assets/3f36193a-23da-4054-9b90-917fe81b41e7)

#### Output
![avg_salary_out](https://github.com/user-attachments/assets/4d4661f5-4350-49e0-a6e4-ae0ce426643f)

---

### ✔ 3. Employee name + department name where name starts with 'm'

#### Code
![starts_m_cmd](https://github.com/user-attachments/assets/013d3f93-ee00-4272-897e-b49d8924debe)

#### Output
![starts_m_out](https://github.com/user-attachments/assets/9d289658-ba32-4dff-af50-e8f5974ef06a)

---

### ✔ 4. Add `bonus` = salary * 2

#### Code
![bonus_cmd](https://github.com/user-attachments/assets/1b0366c4-3808-48c4-b8a5-42e72db11a61)

#### Output
![bonus_out](https://github.com/user-attachments/assets/7fed9050-651f-4712-8844-9ccf922e3ea5)

---

### ✔ 5. Reorder columns as (employee_id, employee_name, salary, State, Age, department, bonus)

#### Code
![reorder_cmd](https://github.com/user-attachments/assets/9f7cb28c-b27b-4e34-96a8-7e102110210d)

#### Output
![reorder_out](https://github.com/user-attachments/assets/a621e4b4-0763-4cc7-986d-21b7a4460949)

---

### ✔ 6. Inner, Left, Right joins (dynamic) — show outputs

#### Inner join input:
![inner_cmd](https://github.com/user-attachments/assets/3ab3a5a8-c372-4b9a-910a-5b1a8ff87d08)

#### Inner join output:
![inner_out](https://github.com/user-attachments/assets/be428178-9d41-48ac-9927-561d1bb7ee2d)

#### Left join input:
![left_cmd](https://github.com/user-attachments/assets/2a9ccab7-6f0b-4086-8067-f71af3b8ef03)

#### Left join output:
![left_out](https://github.com/user-attachments/assets/869f9955-9345-485f-b2e4-474b5e89ef0e)

#### Right join input:
![right_cmd](https://github.com/user-attachments/assets/645d88f9-71ec-4b7a-8941-4101097cb289)

#### Right join output:
![right_out](https://github.com/user-attachments/assets/cb53eb89-c15e-4559-bbf2-5a328c10202c)

---

### ✔ 7. Replace `State` with `country_name` in `employee_df`

#### Code
![country_replace_cmd](https://github.com/user-attachments/assets/374be50c-29f8-4878-8756-f5ee0ce13ae8)

#### Output
![country_replace_out](https://github.com/user-attachments/assets/7063630c-a1c7-4954-9d0e-ee2f0e2c00b3)

---

### ✔ 8. Convert column names to lowercase (dynamic) and add `load_date`

#### Code
![lowercase_cmd](https://github.com/user-attachments/assets/919afeac-c25e-40e6-91dc-f03f85d024d4)

#### Output
![lowercase_out](https://github.com/user-attachments/assets/8c887079-a764-4a74-9fd3-8adbee4a5d6c)

---

## Notes & Next Steps

- This markdown file includes dataset definitions, PySpark code snippets, and the screenshots provided as visual outputs.  

---


