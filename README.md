# 💳 Financial Loan Dashboard (Tableau)

### 📌 Project Overview

The **Financial Loan Dashboard** is an interactive **Tableau-based analytics project** built to analyze loan performance, funding distribution, and repayment behavior across different borrower segments, loan grades, and geographic regions.

This project visualizes the data of a lending organization (modeled after **Lending Club Loan Data**) and provides a **real-time financial performance snapshot**, helping business stakeholders assess loan quality, risk exposure, and funding patterns.
<img width="1919" height="1016" alt="image" src="https://github.com/user-attachments/assets/fed2eb48-6611-496b-b38b-47c1922c687a" />

---

## 🎯 Objectives

The primary goals of this dashboard are:

* To analyze the **overall loan portfolio performance** by comparing funded amounts, repayments, and issued loans.
* To differentiate between **good loans** (fully paid or on track) and **bad loans** (defaulted or charged-off).
* To visualize loan distribution **by purpose, term, grade, and geography**.
* To identify patterns and trends in loan issuance over time.
* To provide actionable insights for **financial risk analysis** and **decision-making**.

---

## 🧾 Dataset Description

The dashboard is built using the **Financial Loan Data.csv** file, which contains transaction-level information about issued loans, borrower details, and loan performance.

| **Column Name** | **Description**                                                                         |
| --------------- | --------------------------------------------------------------------------------------- |
| `Loan_ID`       | Unique identifier for each loan                                                         |
| `Loan_Status`   | Indicates if the loan is *Good* (Fully Paid / Current) or *Bad* (Charged-Off / Default) |
| `Loan_Amount`   | Principal amount issued for the loan                                                    |
| `Funded_Amount` | Amount funded by investors                                                              |
| `Total_Payment` | Total amount repaid by the borrower                                                     |
| `Term`          | Duration of the loan (36 or 60 months)                                                  |
| `Purpose`       | Purpose of the loan (debt consolidation, small business, etc.)                          |
| `Grade`         | Credit grade assigned to the borrower (A–G)                                             |
| `State`         | U.S. state of the borrower                                                              |
| `Issue_Date`    | Loan issuance date                                                                      |
| `Interest_Rate` | Annual percentage rate charged on the loan                                              |
| `Installment`   | Monthly payment amount                                                                  |
| `Emp_Length`    | Borrower’s employment length (in years)                                                 |
| `Annual_Income` | Reported annual income of the borrower                                                  |

---

## ⚙️ Data Preparation

Data was preprocessed and cleaned before loading into Tableau:

1. **Removed null and duplicate records.**
2. **Standardized date fields** (`Issue_Date`) for trend analysis.
3. **Derived categorical fields**:

   * *Loan Type* = Good Loan / Bad Loan (based on `Loan_Status`).
   * *Year of Issue* extracted from `Issue_Date`.
4. Created **calculated fields** for:

   * `Good Loan %` and `Bad Loan %`
   * `Total Funded Amount` and `Total Payment`
   * Loan term segmentation (`36 months`, `60 months`)

---

## 📊 Dashboard Components

### 1️⃣ **KPI Summary Section**

Displays overall loan statistics:

| Metric                     | Value                 |
| -------------------------- | --------------------- |
| **Total Loan Issued**      | 39,717                |
| **Total Funded Amount**    | $434,810,325          |
| **Total Payment Received** | $482,704,394          |
| **Good Loans**             | 85.83% (34,090 loans) |
| **Bad Loans**              | 14.17% (5,627 loans)  |

These metrics provide a quick snapshot of the organization’s lending performance.

---

### 2️⃣ **Loan Issued Trend**

* Line chart visualizing the **monthly growth of loans issued** over time.
* Indicates consistent increase in loan issuance — showing business growth and lending confidence.

---

### 3️⃣ **Loan Purpose Analysis**

#### **Bad Loans by Purpose**

* Horizontal bar chart displaying which loan purposes have the highest number of defaults.
* **Top causes:** Debt Consolidation, Credit Card, and Small Business Loans.

#### **Good and Bad Loan % by Purpose**

* Side-by-side comparison showing the **percentage of good vs bad loans** for each purpose.
* Example:

  * *Debt Consolidation:* 39.97% Good | 6.97% Bad
  * *Home Improvement:* 12.53% Good | 1.85% Bad

---

### 4️⃣ **Geographic Analysis**

#### **State-Wise Loan Issued Map**

* Filled map (choropleth) visualizing total loans issued by U.S. state.
* States like **CA, TX, FL, and NY** have the highest loan issuance, reflecting dense borrower regions and active lending operations.

---

### 5️⃣ **Loan Term & Grade Analysis**

#### **Term-Wise Loan Distribution**

* Donut chart showing the percentage of loans by term:

  * **36 Months:** 75.88%
  * **60 Months:** 24.12%

#### **Grade-Wise Good Loan %**

* Bar chart visualizing the proportion of good loans by credit grade.
* **Grades A–C** maintain the highest repayment reliability, while **Grades F–G** show elevated default risk.

---

## 💡 Insights

* **Good Loans (85.83%)** dominate the portfolio, suggesting strong borrower creditworthiness.
* **Debt Consolidation** loans are the most common purpose (≈45% of total loans), but also show the highest default rate.
* **Western and Southern U.S.** states lead in total loan issuance.
* **Longer-term loans (60 months)** tend to have higher default probability than 36-month loans.
* **Higher grades (A–C)** correspond to significantly lower default rates, confirming grading effectiveness.

---

## 🧠 Key Performance Indicators (KPIs)

| KPI                     | Formula                                    |
| ----------------------- | ------------------------------------------ |
| **Good Loan %**         | (Count of Good Loans ÷ Total Loans) × 100  |
| **Bad Loan %**          | (Count of Bad Loans ÷ Total Loans) × 100   |
| **Total Funded Amount** | SUM(`Funded_Amount`)                       |
| **Total Payment**       | SUM(`Total_Payment`)                       |
| **Loan Growth Trend**   | Calculated via `Index()` over `Issue_Date` |

---

## 🛠️ Tools & Technologies

| Tool                                 | Purpose                              |
| ------------------------------------ | ------------------------------------ |
| **Tableau Desktop (Public Edition)** | Dashboard creation and visualization |
| **Microsoft Excel / CSV**            | Data source and pre-processing       |
| **Calculated Fields & Filters**      | Data modeling and interactivity      |
| **Mapbox Integration**               | Geographic visualization             |
| **KPIs & Parameters**                | Dynamic insights and drill-downs     |

---

## 🧩 Skills Demonstrated

* Data Cleaning and Feature Engineering
* Data Visualization and Dashboard Design
* KPI Calculation and Trend Analysis
* Risk Segmentation (Good vs Bad Loans)
* Geographic and Categorical Analytics
* Business Reporting using Tableau

---

## 📁 Deliverables

* **Dataset:** `Financial Loan Data.csv`
* **Tableau Workbook:** `Financial Loan Dashboard.twbx`


---

## 🚀 Insights for Business Use

* Helps **lending institutions** identify high-risk loan categories and geographies.
* Assists **credit analysts** in understanding repayment behavior by grade and purpose.
* Enables **executive reporting** through KPI tracking of portfolio growth and profitability.

---

## 👨‍💻 Author

**Puneeth Vijay Krishna Samarla**
M.S. in Information Science (Machine Learning) — University of Arizona
📧 [puneethvks9@email.com](mailto:puneethvks9@email.com)
🔗 [LinkedIn](https://www.linkedin.com/in/puneeth-samarla)

