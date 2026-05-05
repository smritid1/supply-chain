# Supply Chain Analysis in Power BI – Make vs Buy Decision Analytics

## Project Overview

This project focuses on performing a **Make vs Buy Analysis** using **Power BI** for a fictitious company called **Tenate Industries**, which sells replacement parts for industrial pizza ovens.

The objective of this project is to help the company determine whether it is more cost-effective to:
- Manufacture products internally (**Make Option**)
- Purchase products from external suppliers (**Buy Option**)

The project analyzes supplier quotations, manufacturing estimates, production volumes, equipment investment costs, and scenario analysis to support strategic supply chain decisions.

---

# Business Problem

A **Make vs Buy Decision** is the process of choosing between:
- Manufacturing a product internally
- Purchasing the product from an external supplier


This project focuses primarily on the **cost analysis aspect** of the decision-making process.

---

# Important DAX Calculations

## Extended Cost
```DAX
Extended Cost = Quotes[Unit_Cost] * Quotes[Volume]
```

---

## Full Cost
```DAX
Full Cost = Quotes[Extended Cost] + Quotes[Non_recurring_expenses]
```

---

## Equipment Needed
```DAX
Equipment Needed =
ROUNDUP(
(Scenario Volume - Existing Capacity)
/ Equipment Capacity,
0
)
```

---

# Key Findings

## Supplier Quote Analysis

- Part Number **P0380** had:
  - **20 supplier price quotes**

- Supplier analysis is critical for:
  - Cost optimization
  - Vendor selection
  - Negotiation strategy

---

## Unit Cost vs Volume Relationship

### Observation
As production volume increases:
- Unit cost generally decreases

### Reason
- Economies of scale
- Bulk manufacturing efficiencies

---

## Lowest Quoted Unit Cost

| Part Number | Volume | Lowest Unit Cost |
|---|---|---|
| P9091 | 50,000 Units | 12.15 |

---

## Lowest Full Cost Supplier

| Part Number | Volume | Supplier | Full Cost |
|---|---|---|---|
| 0622 | 5,000 Units | UCell | 68,041.26 |

---

## Scenario Volume Analysis

### Key Insight
A dynamic scenario analysis tool helps evaluate:
- Production uncertainty
- Demand fluctuation
- Supplier pricing thresholds

---

## Important Observation

For product **P0604**:
- Ordering slightly above **50,000 units**
  resulted in a lower total full cost

### Why?
The lower unit cost at higher volume outweighed the additional purchase quantity cost.

---

## Spain Sales Analysis

- Decoration category accounted for:
  - **19.72%** of total sales quantity in Spain

---

# Business Challenges Identified

## 1. Demand Uncertainty
- Forecasted demand often changes
- Marketing projections may be inaccurate

---

## 2. Supplier Cost Variability
- Different suppliers quote significantly different prices
- Volume impacts pricing heavily

---

## 3. Capacity Constraints
- Existing manufacturing capacity may not meet demand
- Additional equipment investment may be required

---

## 4. Hidden Costs
- Non-recurring expenses can drastically affect decisions
- Low unit cost alone can be misleading

---

# Recommendations

## Supplier Strategy
- Compare suppliers based on:
  - Full Cost
  - Not only Unit Cost

- Build strong supplier relationships for faster quote turnaround

---

## Inventory & Production Planning
- Use scenario analysis for uncertain demand
- Prepare for multiple production volume possibilities

---

## Manufacturing Strategy
- Utilize existing equipment before investing in new machinery
- Consider incremental costs only

---

## Data & Analytics
- Use dynamic Power BI models instead of spreadsheets
- Implement parameter-driven scenario analysis
- Build interactive dashboards for decision-makers

---

# Dashboard Features

## Buy Option Dashboard
- Supplier comparison
- Unit cost trends
- Full cost analysis
- Quote analysis

---

## Make Option Dashboard
- Internal manufacturing cost analysis
- Equipment investment simulation
- Capacity analysis
- Incremental cost calculation

---

## Scenario Analysis Dashboard
- Dynamic production volume parameter
- Full cost simulation
- Volume sensitivity analysis

---

# Conclusion

This project demonstrates how Power BI can be used to create advanced supply chain decision-making tools.

The analysis helps businesses:
- Optimize supplier selection
- Reduce manufacturing costs
- Improve production planning
- Analyze uncertainty dynamically
- Make data-driven make vs buy decisions

The project also highlights the importance of:
- Full Cost analysis
- Scenario modeling
- Capacity planning
- Supplier evaluation

