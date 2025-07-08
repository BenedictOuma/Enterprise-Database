# Retail Sales Database & Excel Dashboard Project

## **Project Overview**
This project is a **Retail Sales Analysis** system built in **SQL Server Management Studio (SSMS)** using T-SQL. It simulates a retail business scenario — tracking **customers**, **orders**, **sales**, **products**, and **employees**. The database supports deep business insights including **revenue analysis**, **customer behavior**, **product performance**, and **inventory levels**. These insights were **visualized in Excel** using data imported directly from SQL Server.

---

## **Key Components**

### **1. Database Creation**
- **Database:** `RetailSales`
- **Tables:** `Customers`, `Suppliers`, `Products`, `Employees`, `Orders`, `Sales`
- **Constraints:** Primary Keys, Foreign Keys, and `CHECK` constraints implemented for data integrity.
- **Auto-incrementing IDs:** Used `IDENTITY(start, increment)` in SQL Server.

---

### **2. Data Insertion**
Populated realistic sample data including:
- 26 fictional **customers** (football-themed).
- 7 **suppliers**.
- 9 **employees** with various roles.
- **Orders data** (imported from CSV).
- **Sales data** generated only for **‘Delivered’** orders.

---

### **3. Relationships & Constraints**
- **Foreign Keys:**
  - Orders reference `Customers` and `Products`
  - Products reference `Suppliers`
  - Sales reference `Orders` and `Employees`
- **Indexing:** Clustered indexes created on all primary keys and key foreign columns to improve performance.

---

## **Business Logic & Analysis**

### **Sales Commission & Revenue Calculation**
- Calculated using:
  - `OrderAmount = Quantity * ProductPrice`
  - `SaleAmount = OrderAmount + ShippingFee`
  - `Commission = 5% of SaleAmount` (only if status = 'Delivered')

### **Performance & Reporting via CTEs (Common Table Expressions)**
1. **Employee Commission & Sales Revenue**
2. **Top Spenders & Frequent Buyers**
3. **Product Sales Ranking**
4. **Inventory Level Tracker (Remaining Stock)**
5. **Monthly Sales Trend (for Business Growth)**
6. **Customer Segmentation via Buying Behavior**

---

## **Excel Integration**

### **Connection to SQL Server:**
Data was imported into Excel via:
- `Data` > `Get Data` > `From Database` > `From SQL Server Database`

### **Visualizations Created in Excel:**
1. **Top 3 Customers by Spend** (Bar/Column Chart)
2. **Frequent Buyers** (Ranking Table or Heatmap)
3. **Best-Selling Products** (Pie/Bar Chart)
4. **Inventory Remaining vs. Sold** (Clustered Bar)
5. **Monthly Sales Trend** (Line Graph)
6. **Employee Sales Performance** (KPI Cards & Charts)

---

##  **Tools Used**
- **SQL Server Management Studio (SSMS)**
- **T-SQL** for querying
- **Microsoft Excel** for reports and dashboards

---

## **Key Takeaways**
- Built a realistic **relational database** for retail operations.
- Applied **CTEs and joins** for business analytics.
- Implemented **indexing** for performance.
- Integrated **SQL with Excel** for live dashboards.
- Delivered insights for **sales, inventory, and customer behavior**.

---

## **Future Improvements**
- Add stored procedures for automation.
- Enable refresh via Power Query in Excel.
- Explore Power BI for richer visuals.
- Introduce role-based access or web app integration.
