## 🏨 LuxurStay Hotels - Room Service Analysis (SQL Practical Exam)

### 📋 Project Overview

This SQL-based project was designed to help LuxurStay Hotels identify the root causes of slow room service in their branches across the globe. Management noticed a decline in customer satisfaction—falling below their benchmark rating of 4.5—and asked for data-driven insights to guide improvements.

The analysis was performed across three interconnected tables:

* `Branch` – Contains information about each hotel branch.
* `Request` – Logs customer room service requests and ratings.
* `Service` – Describes the type of service requested.

---

### 🧠 Tasks Completed

#### ✅ **Task 1: Clean Branch Data**

We validated and cleaned the `Branch` table based on strict data integrity rules. This included:

* Replacing invalid or missing values
* Converting data types (e.g., strings to integers)
* Standardizing and sanitizing text fields

**Output:** A cleaned DataFrame called `clean_branch_data`.

#### ✅ **Task 2: Service Time Analysis**

We calculated the **average** and **maximum** time taken to fulfill room service requests, grouped by both service and branch.

**Output Columns:**

* `service_id`
* `branch_id`
* `avg_time_taken`
* `max_time_taken`

**Output:** A DataFrame named `average_time_service`.

#### ✅ **Task 3: Targeted Services in EMEA and LATAM**

We filtered for branches located in **EMEA** and **LATAM** that offered either **Meal** or **Laundry** services. This helps management prioritize improvements in regions where complaints were common.

**Output Columns:**

* `description` (service)
* `branch_id`
* `location`
* `request_id`
* `rating`

**Output:** A DataFrame named `target_hotels`.

#### ✅ **Task 4: Identify Low-Rated Services**

We found all `branch_id` and `service_id` combinations where the **average customer rating** fell below the 4.5 satisfaction target.

**Output Columns:**

* `branch_id`
* `service_id`
* `avg_rating` (rounded to 2 decimal places)

**Output:** A DataFrame named `average_rating`.

---

### 💻 Tech Stack

* **SQL** (PostgreSQL-style queries)
* **DataCamp Workspace** (or any SQL-enabled environment)
* **Relational Schema** with normalized tables

---

### 📎 Notes

* All cleaning and filtering used **only the original raw data** unless otherwise specified.
* Regex (`~`) and type casting were used to prevent errors when validating data types.
* Aliasing (`WITH ... AS`) was used to match naming requirements from the tasks.

---

### 🙌 Author

Ron, a data analyst in training — proudly fighting off dirty data and SQL bugs like a boss 🐍💪

---
MIT License

Copyright (c) 2025 Ron

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

