# Index-Match-
shivamssharma86@gmail.com

📊 Excel INDEX & MATCH Lab – Sales Analysis
📌 Project Overview

This project demonstrates practical usage of INDEX and MATCH functions in Microsoft Excel to perform dynamic lookups, calculations, and analysis on a sales dataset.

The lab focuses on replacing hard-coded references and improving flexibility compared to traditional lookup functions.

📂 Dataset Description
📄 Worksheet: SalesData
ProductID	Product	Category	Jan	Feb	Mar	Apr	May
101	PRODA	Electronics	120	130	140	150	160
102	PRODB	Furniture	150	160	170	180	190
103	PRODC	Electronics	200	210	220	230	240
104	PRODD	Clothing	90	100	110	120	130
105	PRODE	Furniture	220	230	240	250	260
106	PRODF	Electronics	130	140	150	160	170
🧠 Exercise Questions & Solutions
✅ 1. Sales for Product C in March

Goal: Retrieve March sales for PRODC.

=INDEX(D2:H7, MATCH("PRODC", B2:B7, 0), MATCH("Mar", D1:H1, 0))


✔ Result: 220

✅ 2. Category for Product E

Goal: Find the category of PRODE.

=INDEX(C2:C7, MATCH("PRODE", B2:B7, 0))


✔ Result: Furniture

✅ 3. Maximum Sales for Product B (All Months)

Goal: Identify the highest monthly sales for PRODB.

=MAX(INDEX(D2:H7, MATCH("PRODB", B2:B7, 0), 0))


✔ Result: 190

✅ 4. Month with Maximum Sales for Product A

Goal: Find which month has the highest sales for PRODA.

=INDEX(D1:H1, MATCH(MAX(INDEX(D2:H7, MATCH("PRODA", B2:B7, 0), 0)), INDEX(D2:H7, MATCH("PRODA", B2:B7, 0), 0), 0))


✔ Result: May

✅ 5. Total April Sales for Electronics Category

Goal: Sum April sales for all Electronics products.

=SUMIF(C2:C7, "Electronics", INDEX(D2:H7, 0, MATCH("Apr", D1:H1, 0)))


✔ Result: 540

✅ 6. Average Sales for Product D

Goal: Calculate average monthly sales for PRODD.

=AVERAGE(INDEX(D2:H7, MATCH("PRODD", B2:B7, 0), 0))


✔ Result: 110

✅ 7. Sales for Product ID 105 in May

Goal: Lookup May sales using ProductID.

=INDEX(D2:H7, MATCH(105, A2:A7, 0), MATCH("May", D1:H1, 0))


✔ Result: 260

✅ 8. Dynamic Product & Month Lookup

Goal: Allow user input for Product and Month.

📌 Assumptions

Product input in cell K2

Month input in cell K3

=INDEX(D2:H7, MATCH(K2, B2:B7, 0), MATCH(K3, D1:H1, 0))


✔ Fully dynamic and reusable formula

🚀 Key Excel Skills Demonstrated

✔ INDEX function (single & array use)

✔ MATCH for row & column identification

✔ Two-way lookups

✔ Dynamic formulas

✔ Nested functions (INDEX + MATCH + MAX + SUMIF)

✔ Analysis without helper columns
