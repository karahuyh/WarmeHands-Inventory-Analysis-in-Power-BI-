# WarmeHands Inventory Analysis in Power-BI

Inventory analysis is a management technique that can help company optimizes inventory control. For example, help with reducing storage expenses, item costs, and unused goods and to increase profit.

## The Dataset
The WarmeHands dataset contains six (6) tables including items IDs, description, initial stock quantities, individual orders with their respective quantities and dates, order country of precedence, and price.

## Inventory calculations and methods
- **Revenue**: Amount of money a company receives in exchange for its goods and services. To calculate Revenue: Revenue = Quantity of units sold * selling price.
- **Cost of goods sold (COGS)**: Cost of producing or acquiring products that a company sells in a determined period. To calculate COGS in this case study, COGS = raw_material + factory_labor + factory_equipment_rent.
- **Gross Profit**: The amount resulting after subtracting costs associated with making or acquiring products. To calculate Gross Profit: Gross Profit = Revenue - COGS.
- **Average Inventory Value**: The value of an item during a specific period that accounts for seasonal fluctuations. To calculate AIV: Average inventory value = (Starting value + Ending Value) / 2.
- **Inventory Turnover**: A ratio that shows how often a company uses its supply of goods during a given period. To calculate IT: Inventory Turnover: COGS / Average value of inventory.

## Data Cleaning 
| Table  | Errors Description | Cleaning description |
| ------------- | ------------- |------------- |
| **Price**  | Has errors with its values | In Power Query Editor -> rename the column headers -> Remove duplicate rows -> remove "$$" by Find-Replace -> change from Text to Decimal Number -> change to Currency data type. |
| **Stock** | Blank space in SKU-IDs  | In Power Query Editor -> remove space by Find-Replace. |
| **categories** | Prefix "SKU-"  | Remove the value, Find-Replace option. |
| **Orders** | Duplicated Countries  | In Power Query Editor -> remove duplicated -> hide the uninformative Country table |
| **categories** | Prefix "SKU-"  | Remove the value, Find-Replace option. |
| **categories** | Prefix "SKU-"  | Remove the value, Find-Replace option. |

## Visualisation
### Quantity, Retail Price by Items, Calculating COGS, Revenue and Profit
Outer Join Price and Stock tables before doing this step
Import another Excel file called "category"

Table and Column chart comprehensively show Quantity, Retail Price by Items, Country and Category 

<div align="center">
</div>


### Sales by Years
The viz shows the most sold and least sold item of 2021, helps the company understands more about its product offerings and their profit generation ability. 

"Grow a Flytrap or Sunflower in Tin" is the most sold item of 2021, and it accounts for 10.85% of the total amount of stock inventory and around 5 items account for 0% which did not generate sales.

<div align="center">
</div>
### Revenue and Class


### ABC Analysis
1. Item Revenue
2. Calculate the percentage they present from the total revenue
3. Sort the column in descending order to allow the computation of a cumulative increase
4. Classify the items according to a rule of how many the cover of total revenue

**A items** = Cover up to seventy percent of total revenue

**B items** = Cover the following twenty %

**C items** = Represent the remaining %


