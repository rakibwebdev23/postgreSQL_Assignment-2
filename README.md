---

### 1. What is PostgreSQL?

PostgreSQL হলো একটি শক্তিশালী ও ওপেন সোর্স রিলেশনাল ডেটাবেস ম্যানেজমেন্ট সিস্টেম (RDBMS), যা ডেটা নিরাপদভাবে সংরক্ষণ, পরিচালনা এবং সহজে অ্যাক্সেস করার জন্য ব্যবহৃত হয়। এটি এমন একটি উন্নত সফটওয়্যার যা প্রতিষ্ঠানের বা অ্যাপ্লিকেশনের সব গুরুত্বপূর্ণ তথ্যকে সুন্দরভাবে গুছিয়ে রাখে এবং যখন প্রয়োজন তখন দ্রুত সেই তথ্য খুঁজে বের করতে সাহায্য করে।

---

### 2. What is the purpose of a database schema in PostgreSQL?

PostgreSQL-এ (Schema) হলো একটি লজিক্যাল স্ট্রাকচার, যার মাধ্যমে ডেটাবেসের বিভিন্ন উপাদান যেমন টেবিল, ভিউ, ইনডেক্স, ফাংশন, ও সিকোয়েন্স-গুলোকে গুছিয়ে ও সংগঠিতভাবে রাখা যায়।

একটি ডেটাবেসে অনেক টেবিল, ভিউ, ফাংশন ইত্যাদি থাকতে পারে। (Schema) ব্যবহার করে এই অবজেক্টগুলোকে তাদের কার্যকারিতা অনুযায়ী আলাদা আলাদা গ্রুপে ভাগ করা যায়।

উদাহরণ: public, admin, sales এই নামে স্কিমা থাকতে পারে, যেখানে আলাদা আলাদা টেবিল ও ফাংশন থাকবে, যেমন admin.users, sales.customers ইত্যাদি।

---

### 3. What is the difference between the VARCHAR and CHAR data types?

1. VARCHAR(n): প্রয়োজন অনুযায়ী যতটুকু জায়গা লাগে ঠিক ততটুকুই জায়গা নেয়।
2. CHAR(n): সবসময় ঠিক n ক্যারেক্টার জায়গা নেয়, কম হলে ফাঁকা (space) জায়গা দিয়ে পূরণ করে।

উদাহরণ:

```sql
name VARCHAR(50)
code CHAR(10)

### 4. How can you modify data using UPDATE statements?

UPDATE কমান্ড দিয়ে একটি টেবিলের নির্দিষ্ট কোনো ডেটা পরিবর্তন করা যায়। তবে আপনাকে নির্দিষ্ট করে বলতে হবে টেবিলের কোন ডেটা পরিবর্তন করতে চান। এজন্য আমরা `WHERE` ক্লজ ব্যবহার করি।  

`WHERE` ছাড়া UPDATE করলে টেবিলের সবগুলো ডেটা পরিবর্তন হয়ে যাবে, যা সাধারণত না করারই উচিত।

উদাহরণ:

```sql
UPDATE students SET age = 20 WHERE student_id = 1;

### 5. How can you calculate aggregate functions like COUNT(), SUM(), and AVG() in PostgreSQL?

PostgreSQL-এ অ্যাগ্রিগেট ফাংশনগুলো (Aggregate Functions) ব্যবহার করে অনেকগুলো রেকর্ডের ওপর গণনা করে একটি সারাংশ মান পাওয়া যায়।

সবচেয়ে সাধারণ ফাংশনগুলো হলো: COUNT(), SUM(), এবং AVG()।

```sql
SELECT COUNT(*) FROM employees;
SELECT SUM(salary) FROM employees;
SELECT AVG(salary) FROM employees; aita sundor kore readme file kore dao serial wise sajaba

-----------------------------------------------

