📌 Project Overview

This project focuses on analyzing Amazon sales data to uncover insights into product performance, customer behavior, and revenue trends. The analysis results are visualized through an interactive dashboard to support data-driven decision-making.




🎯 Objectives

Perform exploratory data analysis (EDA) on Amazon sales data.

Identify key sales trends, top-performing products, and revenue sources.

Develop an interactive dashboard to visualize insights for stakeholders.






📊 Dataset

The dataset includes details such as:

Order ID, Product Name, Category

Sales, Profit, Quantity.







🛠️ Steps Involved

Data Collection: Gather raw sales data.

Data Cleaning: Handle missing values, data formatting, and inconsistencies.

Exploratory Data Analysis (EDA): Identify key patterns and trends.

Visualization: Build an intuitive dashboard.

Insight Generation: Extract actionable insights for business improvement.






🖥️ Dashboard Features

Product Performance: Track top-selling and low-performing products.

Revenue Trends: Monthly, quarterly, and yearly analysis.

Customer Insights: Breakdown by region, purchase behavior.

Profit Analysis: Visualize profit margins across categories.





![image](https://github.com/user-attachments/assets/7d14fbbc-4068-4abf-9f11-3caa813f6b37)


This dashboard provides an overview of Amazon sales performance with interactive visual insights. Let’s break it down:


🔹 Key Metrics Overview (Top Section)
5.79K — Total Sales Amount
8 — Total Units Sold
2 — Seller Count

🔹 Status Filters


Allows filtering by:

Shipped
Shipped - Delivered to Buyer

🔹 Sales Breakdown by City
Displays sales distribution across top cities like Dombivli, Jagtial, and Bengaluru, with sales amounts shown in orange bars.
Helps spot high-demand areas.


🔹 Sales Breakdown by State
Highlights top-performing states, with Maharashtra leading, followed by Telangana and Andhra Pradesh.
Useful for regional performance analysis.


🔹 Sales Over Time (Bottom Chart)
A trend line tracking units sold over time.
The declining slope may hint at seasonal effects, stockouts, or marketing dips.


🔹 Product List (Left Sidebar)
Shows key products like Boys Belts, Baby Carriers, and Boys Dungarees with visuals and quick info.
Selecting a product filters data for detailed analysis.


![image](https://github.com/user-attachments/assets/5359f3ac-e053-4076-96a5-a8181dda5e21)



Sql Tasks Performed:


# Amazon-Sales-Analytics
SQL Queries 

-----------------------------------------------------------------------
Check Icon Url = "https://i.postimg.cc/RV3LcN3L/check-2.png"
-----------------------------------------------------------------------
For Sale Icon On - 

SalesOn = var selected = SELECTEDVALUE(Sale_Option[Type)
var _url = "https://drive.google.com/uc?export=view&id=1mcmb1peVHoaU5XL2bYXinZtW9sv2bNG4"
return IF(selected="1",_url)


-----------------------------------------------------------------------

For Units Icon On - 

SalesOn = var selected = SELECTEDVALUE(Sale_Option[Ty[e])
var _url = "https://drive.google.com/uc?export=view&id=1mcmb1peVHoaU5XL2bYXinZtW9sv2bNG4"
return IF(selected="2",_url)

-----------------------------------------------------------------------

Seller Count = CALCULATE([Sale_Units],ALL('amazon-fashion'[Category]))
= var val = CALCULATE(COUNT('amazon-fashion'[seller_id]),CONTAINSSTRING(Amazon[Status],"Delivered"))
Return val

-----------------------------------------------------------------------

Filter Sale = var selecting = SELECTEDVALUE(Sale_Option[Type])
var _units =SUM(Amazon[Qty])
var _sale = SUM(Amazon[Total_Ammount])
return IF(selecting="1",_sale,_units)

-----------------------------------------------------------------------

Color Orange - #FF9F10
Background Color - #F8F8F8
White Color -  #FFFFFF



Return_Units = var val= CALCULATE([Sale_Units],CONTAINSSTRING(Amazon[Status],"Return"))
return IF(val=BLANK(),0,val)

Reviews = var val = COUNT('amazon-fashion'[no__of_reviews])
return IF(ISBLANK(val),0)

Sale_Ammount = var val = SUM(Amazon[Total_Ammount])
return if(ISBLANK(val),0)

Sale_Units = var selecting = SELECTEDVALUE(Sale_Option[Type])
var _units =SUM(Amazon[Qty])
var _sale = SUM(Amazon[Total_Ammount])
return IF(selecting="1",_sale,_units)

Sale_Option =
 DataTable("Name", STRING,"Type", STRING,{{"1","Sales"},{"2","Units"}})   

Sale_Units = var selecting = SELECTEDVALUE(Sale_Option[Type])
var _units =SUM(Amazon[Qty])
var _sale = SUM(Amazon[Total_Ammount])
return IF(selecting="1",_sale,_units)

All_Sale = CALCULATE([Sale_Units],ALL('amazon-fashion'[Category]))

Order_Counts = var val = CALCULATE(COUNT('amazon-fashion'[seller_id]),CONTAINSSTRING(Amazon[Status],"Delivered"))
return IF(val=BLANK(),"0",val)





🔍 Conclusion

The Amazon Sales Analytics Dashboard effectively uncovers valuable insights into sales performance across products, regions, and time periods. It highlights key trends such as top-performing products, revenue-driving regions, and potential areas for improvement in shipping and product sales. This dashboard enables data-driven decision-making, empowering stakeholders to optimize product strategies, improve logistics, and boost overall profitability.













